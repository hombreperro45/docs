# iOS Compilation / Development Guide

## Environment configuration

The following software needs to be installed:

- XCode
- iOS SDK

The following versions of the operating system are supported:

- iOS 6.0
- iOS 7.0+
- iOS 8.0+
- iOS 9.0+
- iOS 10.0+

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

#### Using the graphical interface

##### For iOS 6 to 8

Open Xcode. Open the following project file `pkg/apple/RetroArch_iOS.xcodeproj` in the Xcode IDE and build (**&#8984;-B**) and run (**&#8984;-R**) it there. Or you can use the command line....

#### For iOS 10 and up

Open Xcode. Open the following project file `pkg/apple/RetroArch_iOS10.xcodeproj` in the Xcode IDE and build (**&#8984;-B**) and run (**&#8984;-R**) it there. Or you can use the command line....

#### Using the command line

##### For iOS 6 to 8

To build a debug build :

    # Build
    xcodebuild -target RetroArch -configuration Debug -project pkg/apple/RetroArch_iOS.xcodeproj
    # Run
    open ./pkg/apple/build/Debug/RetroArch.app/

To build a release build :

    # Build
    xcodebuild -target RetroArch -configuration Release -project pkg/apple/RetroArch_iOS.xcodeproj
    # Run
    open ./pkg/apple/build/Release/RetroArch.app/

##### For iOS 10 and up

To build a debug build :

    # Build
    xcodebuild -target RetroArch -configuration Debug -project pkg/apple/RetroArch_iOS10.xcodeproj
    # Run
    open ./pkg/apple/build/Debug/RetroArch.app/

To build a release build :

    # Build
    xcodebuild -target RetroArch -configuration Release -project pkg/apple/RetroArch_iOS10.xcodeproj
    # Run
    open ./pkg/apple/build/Release/RetroArch.app/

### Packaging RetroArch

### Additional Tips:

## Core Compilation

### Fetching Cores

The easiest way to fetch all the cores is to use libretro-super. Run

    ./libretro-fetch.sh

### Building Cores

The easiest way to build all the cores (for iOS) is to use libretro-super. 

To build iOS 6 to 8-compatible cores, run

    ./libretro-build-ios.sh

To build iOS 9 and up-compatible cores, run

    ./libretro-build-ios9.sh

In case you only want to build one and/or more cores instead of all, you can specify the cores you want to build after the first command in no particular order. E.g.:

    ./libretro-build-ios.sh snes9x2010 fceumm

Once finished, you can find the libretro cores inside directory `dist/ios`.
