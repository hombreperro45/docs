# Sega Dreamcast (Redream)

## Background

redream is a work-in-progress SEGA Dreamcast emulator written in C for Mac, Linux and Windows.

**This core requires OpenGL 3.3 or higher in order to work.** RetroArch's video driver must be set to OpenGL. Go to Settings -> Driver. If the ‘video driver’ is set to something else or than 'gl', switch to ‘gl’, and then restart.

**Note for macOS users**: There is currently no ‘working’ macOS version available. This is because this core requires OpenGL core 3.3 context, and RetroArch on macOS currently does not support this. We will have to add support for this to a future version of RetroArch on macOS before this core will start to work on it.

### Why use this core?

-

### Author(s):

inolen

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/redream.md). Changes are proposed using "Pull Requests."

## See also

-

## License

GPLv3

## Extensions

gdi|chd|cdi

## Database(s)

*RetroArch databases that are associated with the Redream core*

* Sega - Dreamcast

## BIOS

*Required or optional firmware files go in RetroArch's system directory.*

|   Filename    |    Description         |              md5sum              |
|:-------------:|:----------------------:|:--------------------------------:|
| dc/dc_boot.bin  | dc_boot.bin (Dreamcast BIOS) - Required | e10c53c2f8b90bab96ead2d368858623                |
| dc/dc_flash.bin | dc_flash.bin (Date/Time/Language) - Required | dc_flash.bin (md5): 0a93f7940c455905bea6e392dfde92a4 |

## Features

| Feature           | Supported |
|-------------------|:---------:|
| Saves             | ✔         |
| States            | ✕         |
| Rewind            | ✕         |
| Netplay           | ✕         |
| RetroAchievements | ✕         |
| RetroArch Cheats  | ✕         |
| Native Cheats     | ✕         |
| Controllers       | ✔         |
| Multi-Mouse       | ✕         |
| Rumble            | ✕         |
| Sensors           | ✕         |
| Camera            | ✕         |
| Location          | ✕         |
| Subsystem         | ✕         |

The Redream core creates directories named 'redream' in RetroArch's...

* Savefile directory when the core is loaded.
* Statestate directory when the core is loaded.
* Config directory when a Core Override or a Game Override or a Game-options file is saved.
* Input Remapping directory when a Core Remap or a Game Remap is saved.
* Shaders Presets directory when a Core Preset or a Game Preset is saved.

Core Overrides/Remaps/Presets that are saved will be named 'redream'.

Game Overrides/Remaps/Presets and Game-option files will have the same name as the loaded content.

Game data is saved/loaded to and from where the required firmware files are located.  

## Options

The Redream core does not feature core options.

## Controllers

*The Redream core supports the following controller setting(s), bolded controller settings are the default for the specified user(s):*

### User 1 - 16 Device Type(s)

* **RetroPad** - Joypad without analog

* RetroPad w/Analog - Joypad with analog

### Controllers graph

| Redream     | RetroPad                                                       |
|-------------|----------------------------------------------------------------|
| A           | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               |
| X           | ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               |
| Start       | ![RetroPad_Start](images/RetroPad/Retro_Start.png)             |
| D-Pad Up    | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Up.png)            |
| D-Pad Down  | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Down.png)          |
| D-Pad Left  | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Left.png)          |
| D-Pad Right | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Right.png)         |
| B           | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               |
| Y           | ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               |
| L           | ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              |
| R           | ![RetroPad_R2](images/RetroPad/Retro_R2.png)                   |
| Analog      | ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)   |

## Compatibility

Since Redream is a work-in-progress Dreamcast emulator, expect sound issues, general compatibility issues, and a general rough experience.

## External Links

* [Official Repository](https://github.com/inolen/redream) (this core has upstream libretro integration)
* [Report Core Issues Here](https://github.com/inolen/redream/issues)
* [Official Website](http://redream.io/)