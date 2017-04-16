# Windows (Vista and later) Compilation / Development Guide

!!! Warning
    The MinGW toolchain we use in this guide no longer supports targetting Windows XP. Programs compiled with it will fail to   start with it.
    Please refer to one of the MSVC guides for how to target older Windows versions with Visual Studio.

## Environment configuration

We recommend MinGW-W64 from MSYS2. You can download MSYS2 installer from [here](http://msys2.github.io/)

Follow the installation instructions and once finished start MSYS2 shell.

MSYS2 shell is a maintenance shell. We are going to use this shell to install the toolchain and other packages. First order of business is to update MSYS2:

    pacman --noconfirm -Sy
    pacman --needed --noconfirm -S bash pacman pacman-mirrors msys2-runtime

Close MSYS2 shell and start it again, and:

    pacman --noconfirm -Su

Restart MSYS2 once again. In some cases you may find out that the shell starting scripts don't work. If so check the following Note.

!!! Note
    In some cases you may need to update your shortcuts to reflect changes in MSYS2's subsystem. If the shell no longer works properly you need to update your shortcuts with the following targets:

- MinGW-w64 Shell: `MSYS2_ROOT\msys2_shell.cmd -mingw64`
- MinGW-w32 Shell: `MSYS2_ROOT\msys2_shell.cmd -mingw32`
- MSYS2 Shell: `MSYS2_ROOT\msys2_shell.cmd -msys`

Now we can start installing the packages we actually need.

For 32-bit builds:

    pacman -S --noconfirm --needed wget git make mingw-w64-i686-toolchain mingw-w64-i686-ntldd mingw-w64-i686-zlib mingw-w64-i686-pkg-config mingw-w64-i686-SDL2 mingw-w64-i686-libxml2 mingw-w64-i686-freetype mingw-w64-i686-python3 mingw-w64-i686-ffmpeg

For 64-bit builds:

    pacman -S --noconfirm --needed wget git make mingw-w64-x86_64-toolchain mingw-w64-x86_64-ntldd mingw-w64-x86_64-zlib mingw-w64-x86_64-pkg-config mingw-w64-x86_64-SDL2 mingw-w64-x86_64-libxml2 mingw-w64-x86_64-freetype mingw-w64-x86_64-python3 mingw-w64-x86_64-ffmpeg

The NVIDIA CG toolkit package hasn't been updated for a while so we need to download that package manually and install with pacman. You can download the packages from sourceforge at the following locations: [32-bit](http://sourceforge.net/projects/msys2/files/REPOS/MINGW_GCC_4_9/i686/mingw-w64-i686-nvidia-cg-toolkit-3.1-2-any.pkg.tar.xz/download) [64-bit](http://sourceforge.net/projects/msys2/files/REPOS/MINGW_GCC_4_9/x86_64/mingw-w64-x86_64-nvidia-cg-toolkit-3.1-2-any.pkg.tar.xz/download). Alternatively you can use the following commands directly:

For 32-bit builds:

    wget http://sourceforge.net/projects/msys2/files/REPOS/MINGW_GCC_4_9/i686/mingw-w64-i686-nvidia-cg-toolkit-3.1-2-any.pkg.tar.xz/download -O mingw-w64-i686-nvidia-cg-toolkit-3.1-2-any.pkg.tar.xz
    pacman -U mingw-w64-i686-nvidia-cg-toolkit-3.1-2-any.pkg.tar.xz

For 64-bit builds:

    wget http://sourceforge.net/projects/msys2/files/REPOS/MINGW_GCC_4_9/x86_64/mingw-w64-x86_64-nvidia-cg-toolkit-3.1-2-any.pkg.tar.xz/download -O mingw-w64-x86_64-nvidia-cg-toolkit-3.1-2-any.pkg.tar.xz
    pacman -U mingw-w64-x86_64-nvidia-cg-toolkit-3.1-2-any.pkg.tar.xz

Once these packages are installed close MSYS2 shell and open MinGW-w32 shell or MinGW-w64 shell depending on the platform you want to build for.

## RetroArch Compilation
### Building RetroArch

The first step is to obtain RetroArch's source tree.
You can clone the repository directly from [GitHub](https://github.com/libretro/RetroArch)

    git clone https://github.com/libretro/RetroArch.git retroarch

For subsequent builds you will need to pull the changes from the repo

    cd retroarch
    git pull

To compile RetroArch run the following commands inside RetroArch's source tree:

    ./configure
    make clean
    make -j4

For development purposes you might want to run a debug build instead. In such case use the following commands:

    ./configure
    make clean
    make DEBUG=1 GL_DEBUG=1 -j4

After a few minutes you should be able to find retroarch.exe under that directory. To start the newly compiled retroarch you can use: 

   ./retroarch

### Packaging RetroArch

You might not be able to start your own build outside that environment. You might want to try to get all the required DLLs by using the following script:

    for i in $(seq 3); do for bin in $(ntldd -R *exe | grep -i mingw | cut -d">" -f2 | cut -d" " -f2); do cp -vu "$bin" . ; done; done;

If you really want to get the required libraries for distribution or for personal use on other devices and LDD doesn't work for you, then you can try [Dependency Walker](http://www.dependencywalker.com/). 

### Additional Tips:

If you're building frequently you may want to add **ccache** to the mix to speed up the build process: 

For 32-bit builds:

    pacman -S --noconfirm --needed make mingw-w64-i686-ccache

For 64-bit builds:

    pacman -S --noconfirm --needed mingw-w64-x86_64-ccache

Then you have to prepend ccache's directories to your build environment. You can do so by doing this:

For 32-bit builds:

    export PATH=/mingw32/lib/ccache/bin/:$PATH

For 64-bit builds:

    export PATH=/mingw64/lib/ccache/bin/:$PATH

You can add the corresponding line to your *~/.bashrc* to avoid having to type that every time you start your working environment.

From our own buildbot, the times with and without **ccache** are the following:

Without **ccache**:

    real    2m7.645s
    user    0m2.585s
    sys     0m11.527s

With **ccache**:

    real    0m25.466s
    user    0m2.902s
    sys     0m9.952s

You can also strip the debug symbols of the build product to save some space.

    strip -s retroarch.exe

## Core Compilation

### Fetching Cores

Most cores can be built by invoking make inside the core's source tree.
You can find the core on libretro's [GitHUB organization](https://github.com/libretro/). 

We have an all-in-one tool to fetch and compile cores which you can use to streamline the process.
You can obtain the tool by using these commands:

    git clone https://github.com/libretro/libretro-super.git
    cd libretro-super

Then you can fetch one or all the cores by using **libretro-fetch.sh**

Fetch all cores:

    ./libretro-fetch.sh

Fetch one core:

    ./libretro-fetch.sh $corename

!!! Note
     Replace $corename with the name of the core you want to fetch, for example gambatte

### Building Cores

The easiest way to build all the cores is to use **libretro-build.sh** from within libretro-super's source tree:

    ./libretro-build.sh

In case you only want to build one and/or more cores instead of all, you can specify the cores you want to build after the first command in no particular order:

    ./libretro-build.sh snes9x2010 fceumm

Once compilation has finished, you can find the libretro cores inside `dist/windows`.
