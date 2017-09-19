# Atari Lynx (Beetle Handy)

## Background

Beetle/Mednafen Lynx is an Atari Lynx video game system emulator that can be used as a libretro core. Specifically it's a port of Mednafen Lynx which is a fork of Handy.

Author(s): K. Wilkins|Mednafen Team

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/beetle_lynx.md). Changes are proposed using "Pull Requests."

## License

Zlib, GPLv2

## Extensions

lnx

## BIOS

|   Filename    |    Description        |              md5sum              |
|:-------------:|:---------------------:|:--------------------------------:|
|lynxboot.img   |Lynx Boot Image        | fcd403db69f54290b51035d82f835e7b |

## Features

| Saves | States      | Rewind | Netplay | RetroAchievements | RetroArch Cheats | Native Cheats | 
|:-----:|:-----------:|:------:|:-------:|:-----------------:|:----------------:|:--------------|
| yes   |   yes       |  yes   |  no     |       no          |  no              | no            |

| Controllers     | Rumble | Sensors | Camera | Location | Subsystem     |
|:---------------:|:------:|:-------:|:------:|:--------:|:-------------:|
|       yes        |  no   |   no    |  no    |   no     |      no       |

## Options

The Beetle Handy core does not feature core options.

## Controllers

The Beetle Handy core supports one controller setting(s):

* RetroPad

![beetle_lynx_retropad](images/Controllers/beetle_lynx_retropad.png)

| Beetle Handy | [RetroPad](RetroPad)                                           |
|--------------|----------------------------------------------------------------|
| B            | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               |
|              | ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               |
|              | ![RetroPad_Select](images/RetroPad/Retro_Select.png)           |
| Pause        | ![RetroPad_Start](images/RetroPad/Retro_Start.png)             |
| D-pad        | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)               |
| A            | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               |
|              | ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               |
| Option 1     | ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   |
| Option 2     | ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   |
|              | ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              |
|              | ![RetroPad_R2](images/RetroPad/Retro_R2.png)                   |
|              | ![RetroPad_L3](images/RetroPad/Retro_L3.png)                   |
|              | ![RetroPad_R3](images/RetroPad/Retro_R3.png)                   |
|              | ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)   |
|              | ![RetroPad_Right_Stick](images/RetroPad/Retro_Right_Stick.png) |

Supported combinations

* Option 1 + Pause = Flips Screen
* Option 2 + Pause = Restarts game

## Compatibility

| Game                                  | Issue                          |
|---------------------------------------|--------------------------------|
|**RoadBlasters**                       |Graphics glitches. Minor flickering and glitches after starting a race.|

## External Links

* [Libretro Repository](https://github.com/libretro/beetle-lynx-libretro)
* [Report Core Issues Here](https://github.com/libretro/libretro-meta/issues)
* [Official Website](http://mednafen.sourceforge.net/)
* [Official Upstream Downloads](https://mednafen.github.io/releases/)
