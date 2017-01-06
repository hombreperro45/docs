# PlayStation3 Compilation / Development Guide

## Environment configuration

You need the proprietary PlayStation 3 SDK installed. 

## RetroArch Compilation

### Fetching RetroArch

Clone RetroArch's repository from [GitHub](https://github.com/libretro/RetroArch)

    git clone https://github.com/libretro/RetroArch.git retroarch
    cd retroarch

For subsequent builds you only need to pull the changes from the repo

    cd retroarch
    git pull

To update your local copy from the repository run git pull

### Building RetroArch separately

First, you need to compile 'Salamander'. To compile Salamander (for PlayStation3) run:

    make -f Makefile.ps3.salamander
    ./configure
    make clean
    make -j4

Second, to compile RetroArch (for PlayStation3) run:

    make -f Makefile.ps3

!!! Note
    RetroArch on PlayStation3 is statically linked. With statically linked RetroArch, each executable is a separate libretro core instead of the core being separately loaded from a single executable. A pre-existing libretro library needs to be present in the root directory in order to link RetroArch PS3. This file needs to be called 'libretro_ps3.a'.

After a few seconds/minutes you should be able to find a retroarch_ps3.elf and retroarch_ps3.self file under that directory.

### Building RetroArch in bulk

Instead of building each core one by one, you can build all cores as a batch task. Run from the main 'retroarch' directory:

    cd dist-scripts

!!! Note
    Make sure that all the libretro cores that you want to compile are inside the 'dist-scripts' directory.

Once inside this directory, what you need to input now as the parameter depends what kind of PlayStation3 you want to build for. If it's for DEX (debug) PS3s, run :

    ./dist-cores.sh  dex-ps3


If building for 3.55 CFW PS3s and/or higher, run

    ./dist-cores.sh cex-ps3

This process will also automate the packaging process for you.

### Packaging RetroArch

You can add 'pkg' as a parameter in order to make a PKG file (a PlayStation3 packaging file format). For example:

    make -f Makefile.ps3 pkg

This creates an NPDRM package. This can be installed on a debug PlayStation3.

To make a non-NPDRM package that can be installed on a jailbroken/CFW PlayStation3 (PSgroove/PS3 3.55 CFW/etc.), run 

    make -f Makefile.ps3 pkg-signed

If you're using Kmeaw 3.55 firmware, the package needs to be signed. Run 

    make -f Makefile.ps3 pkg-signed-cfw

### Additional Tips:

## Core Compilation

### Fetching Cores

The easiest way to fetch all the cores is to use libretro-super. Run

    ./libretro-fetch.sh

### Building Cores

The easiest way to build all the cores for PlayStation3 is to use libretro-super. Run

    ./libretro-build-ps3.sh

In case you only want to build one and/or more cores instead of all, you can specify the cores you want to build after the first command in no particular order. E.g.:

    ./libretro-build-ps3.sh snes9x2010 fceumm

Once finished, you can find the libretro cores inside 'dist/ps3'.
