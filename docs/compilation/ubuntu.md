# Ubuntu Compilation / Development Guide

## Environment configuration

The easiest route to get into building RetroArch and libretro cores on Ubuntu linux is to use libretro's PPA.
For stable releases you can add the PPA like this:

    sudo add-apt-repository ppa:libretro/stable
    sudo apt-get update

For development work we recommend the testing PPA instead:

    sudo add-apt-repository ppa:libretro/testing
    sudo apt-get update

## RetroArch Compilation
### Building RetroArch

The first step is to obtain RetroArch's source tree.
You can get RetroArch's source tree and it's dependenencies by running the following commands:

    apt-get source retroarch
    apt-get build-dep retroarch