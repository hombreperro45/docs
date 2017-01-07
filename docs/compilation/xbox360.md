# Microsoft Xbox 360 Compilation / Development Guide

!!! warning "Xbox 360 version does not currently compile with latest sources"
    The port will be updated and fixed at a later point in time.

## Environment configuration

The following software needs to be installed:

- Visual Studio 2010 
- Proprietary Microsoft Xbox 360 SDK

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

Open Visual Studio 2010. Open the following solution file `pkg/msvc/RetroArch-Xbox360.sln`.

Select the 'project 'RetroArch Salamander'. build it by pressing F5. 

Next, select the project 'RetroArch'. Build it by pressing F5.

!!! Note
    RetroArch on Xbox 360 is statically linked. With statically linked RetroArch, each executable is a separate libretro core instead of the core being separately loaded from a single executable. A pre-existing libretro library needs to be present in the root directory in order to link RetroArch Xbox 360. This file needs to be called 'libretro_xdk360.lib'. You need to place this file inside the 'target' directory where your executable resides. For instance - if you are building the 'Release' target, the file needs to be moved to `pkg/msvc/Release`.

### Building RetroArch in bulk

Instead of building each core one by one, you can build all cores as a batch task. Run from the main 'retroarch' directory:

    cd dist-scripts

!!! Note
    Make sure that all the libretro cores that you want to compile are inside the 'dist-scripts' directory.

Once inside this directory, run :

    ./xdk360-cores.sh

This process will also automate the packaging process for you.

### Packaging RetroArch


### Additional Tips:

## Core Compilation

### Fetching Cores

The easiest way to fetch all the cores is to use libretro-super. Run

    ./libretro-fetch.sh

### Building Cores

The easiest way to build all the cores (for Xbox 360) is to use libretro-super. Run

    ./libretro-build-xdk360.sh

In case you only want to build one and/or more cores instead of all, you can specify the cores you want to build after the first command in no particular order. E.g.:

    ./libretro-build-xdk360.sh snes9x2010 fceumm

Once finished, you can find the libretro cores inside directory `dist/xdk360`.
