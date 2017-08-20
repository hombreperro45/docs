# Atari Lynx (Handy)

## Background

Handy is an Atari Lynx video game system emulator that can be used as a libretro core.  Handy was the original name of the Lynx project that was started at Epyx and then finished by Atari..

Author(s): K. Wilkins

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/blob/master/docs/library/handy.md). Changes are proposed using "Pull Requests."

## License

Zlib

## Extensions

lnx

## BIOS

|   Filename    |    Description        |              md5sum              |
|:-------------:|:---------------------:|:--------------------------------:|
|lynxboot.img   |Lynx Boot Image        | fcd403db69f54290b51035d82f835e7b |


## Feature Support

These are libretro features, not frontend or standalone emulator features.

##### Features:

| Saves | States      | Rewind | Netplay | RetroAchievements | Cheats |
|:-----:|:-----------:|:------:|:-------:|:-----------------:|:------:|
|  yes  |    yes      | yes    |   no    |       no          |  no    |

| Controllers     | Rumble | Sensors | Camera | Location | Subsystem     |
|:---------------:|:------:|:-------:|:------:|:--------:|:-------------:|
|       no        |   no   |   no    |  no    |   no     |      no       |

## Options

- **Display Rotation** (**None**/90/240): Rotates the display.

## Controllers

The core supports controller setting:

* RetroPad

![Atari Lynx_Gamepad_Diagram](images/Controllers/handy_joypad.png)

| [RetroPad](RetroPad)                                                 | Joypad |
|----------------------------------------------------------------------|--------|
| ![RetroPad_B](images/RetroPad/Retro_B_Round.png)                     | B      |
| ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)                     |        |
| ![RetroPad_Select](images/RetroPad/Retro_Select.png)                 |        |
| ![RetroPad_Start](images/RetroPad/Retro_Start.png)                   | Pause  |
| ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)                     | D-pad  |    
| ![RetroPad_A](images/RetroPad/Retro_A_Round.png)                     | A      |
| ![RetroPad_X](images/RetroPad/Retro_X_Round.png)                     |        |
| ![RetroPad_L1](images/RetroPad/Retro_L1.png)                         | Option 1 |
| ![RetroPad_R1](images/RetroPad/Retro_R1.png)                         | Option 2 |
| ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)                    |        |
| ![RetroPad_R2](images/RetroPad/Retro_R2.png)                         |        |
| ![RetroPad_L3](images/RetroPad/Retro_L3.png)                         |        |
| ![RetroPad_R3](images/RetroPad/Retro_R3.png)                         |        |
| ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)         |        |
| ![RetroPad_Right_Stick](images/RetroPad/Retro_Right_Stick.png)       |        |

Supported combinations

* Option 1 + Pause = Restarts game
* Option 2 + Pause = Flips Screen

## Compatibility

[Handy Compatibility List](https://wiki.libretro.com/index.php?title=Atari_Lynx_Core_Compatibility)

## External Links

* [Libretro Repository](https://github.com/libretro/libretro-handy)
* [Report Issues Here](http://github.com/libretro/libretro-meta/issues)
* [Official Website](http://handy.sourceforge.net/)
