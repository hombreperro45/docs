# Compiling RetroArch on Windows

We recommend MinGW-W64 from MSYS2. You can download MSYS2 installer from here: [1]

Follow the installation instructions and once finished start MSYS2 shell
## Environment setup

MSYS2 shell is a maintenance shell. We are going to use this shell to install the toolchain and other packages. First order of business is to update MSYS2:

    pacman --noconfirm -Sy
    pacman --needed --noconfirm -S bash pacman pacman-mirrors msys2-runtime

Close MSYS2 shell and start it again, and:

    pacman --noconfirm -Su

Restart MSYS2 once again. In some cases you may find out that the shell starting scripts don't work. You may need to update your shortcuts to the following targets:

    MSYS2_ROOT\msys2_shell.cmd -mingw32
    MSYS2_ROOT\msys2_shell.cmd -mingw64
    MSYS2_ROOT\msys2_shell.cmd -msys

Now we can start installing the packages we actually need.

For 32-bit builds:

    pacman -S --noconfirm --needed wget git make mingw-w64-i686-toolchain mingw-w64-i686-pkg-config mingw-w64-i686-SDL2 mingw-w64-i686-libxml2 mingw-w64-i686-freetype mingw-w64-i686-python3 mingw-w64-i686-ffmpeg

For 64-bit builds:

    pacman -S --noconfirm --needed wget git make mingw-w64-x86_64-toolchain mingw-w64-x86_64-pkg-config mingw-w64-x86_64-SDL2 mingw-w64-x86_64-libxml2 mingw-w64-x86_64-freetype mingw-w64-x86_64-python3 mingw-w64-x86_64-ffmpeg

The NVIDIA CG toolkit package hasn't been updated for a while so we need to download that package manually and install with pacman. You can download the packages from sourceforge at the following locations: [32-bit](http://sourceforge.net/projects/msys2/files/REPOS/MINGW_GCC_4_9/i686/mingw-w64-i686-nvidia-cg-toolkit-3.1-2-any.pkg.tar.xz/download) [64-bit](http://sourceforge.net/projects/msys2/files/REPOS/MINGW_GCC_4_9/x86_64/mingw-w64-x86_64-nvidia-cg-toolkit-3.1-2-any.pkg.tar.xz/download). Alternatively you can use the following commands directly:

For 32-bit builds:

    wget http://sourceforge.net/projects/msys2/files/REPOS/MINGW_GCC_4_9/i686/mingw-w64-i686-nvidia-cg-toolkit-3.1-2-any.pkg.tar.xz/download -O mingw-w64-i686-nvidia-cg-toolkit-3.1-2-any.pkg.tar.xz
    pacman -U mingw-w64-i686-nvidia-cg-toolkit-3.1-2-any.pkg.tar.xz

For 64-bit builds:

    wget http://sourceforge.net/projects/msys2/files/REPOS/MINGW_GCC_4_9/x86_64/mingw-w64-x86_64-nvidia-cg-toolkit-3.1-2-any.pkg.tar.xz/download -O mingw-w64-x86_64-nvidia-cg-toolkit-3.1-2-any.pkg.tar.xz
    pacman -U mingw-w64-x86_64-nvidia-cg-toolkit-3.1-2-any.pkg.tar.xz

Once these packages are installed close MSYS2 shell and open MinGW-w32 shell or MinGW-w64 shell depending on the platform you want to build for.

## Building

Clone RetroArch's repository from [GitHub](https://github.com/libretro/RetroArch)  and fetch it's submodules

    git clone https://github.com/libretro/RetroArch.git retroarch
    cd retroarch
    git submodule update --init

This will create a local copy of the RetroArch's source tree into `%MSYS2%/home/%USERNAME%/.` To update your local copy from the repository run git pull and git 
submodule update

To compile RetroArch run:

    ./configure
    make clean
    make -j4

For development purposes you might want to run a debug build instead. In such case use the following commands:

    ./configure
    make clean
    make DEBUG=1 GL_DEBUG=1 -j4

After a few minutes you should be able to find retroarch.exe under that directory. To start the newly compiled retroarch run `./retroarch`

## Packaging

You might not be able to start your own build outside that environment. You might want to try to get all the required DLLs by using the following script:

    for i in $(seq 3); do for bin in $(ldd *exe *dll | grep -i mingw | cut -d\  -f 3); do cp -vu "$bin" . ; done; done

Your mileage may vary. The program we use to find the dependencies **(ld)** seems to be failing lately. Another alternative is to add the toolchain's bin directory to your **PATH**. For 32-bit MinGW add `c:\path\to\msys2\mingw32\bin` and for 64-bit MinGW add `c:\path\to\msys2\mingw64\bin`.

If you really want to get the required libraries for distribution or for personal use on other devices and LDD doesn't work for you, then you can try [Dependency Walker](http://www.dependencywalker.com/). 
