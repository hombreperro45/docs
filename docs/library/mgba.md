# Game Boy Advance (mGBA)

## Background

mGBA is a new emulator for running Game Boy Advance games. It aims to be faster and more accurate than many existing Game Boy Advance emulators, as well as adding features that other emulators lack.

Author(s): endrift

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/mgba.md). Changes are proposed using "Pull Requests."

## License

MPLv2.0

## Extensions

gb|gbc|gba

## BIOS

|   Filename    |    Description       |              md5sum              |
|:-------------:|:--------------------:|:--------------------------------:|
|gba_bios.bin   |Game Boy Advance BIOS - Optional | a860e8c0b6d573d191e4ec7db1b1e4f6 |

## Features

| Saves | States      | Rewind | Netplay | RetroAchievements | RetroArch Cheats | Native Cheats |
|:-----:|:-----------:|:------:|:-------:|:-----------------:|:----------------:|:-------------:|
|  yes  |   yes       | yes    |  no     |        -          |   no             | -             |

| Controllers     | Rumble | Sensors | Camera | Location | Subsystem     |
|:---------------:|:------:|:-------:|:------:|:--------:|:-------------:|
|       no        |  no    |   no    |  no    |   no     |      no       |

## Options

The mGBA core has the following options that can be tweaked from the core options menu. The default setting is bolded.

- Solar sensor level (**0**-10): -
- Allow opposing directional input (**Off**/On): -
- Use BIOS file if found (**On**/Off): -
- Skip BIOS intro (**Off**/On): - 
- Idle loop removal (**Remove Known**/Detect and Remove/Don't Remove): - 

## Controllers

The mGBA core supports one controller setting(s):

* RetroPad

![mgba_retropad](images/Controllers/mgba_retropad.png)

| mGBA                  | [RetroPad](RetroPad)                                           |
|-----------------------|----------------------------------------------------------------|
| B                     | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               |
| Turbo B               | ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               |
| Select                | ![RetroPad_Select](images/RetroPad/Retro_Select.png)           |
| Start                 | ![RetroPad_Start](images/RetroPad/Retro_Start.png)             |
| D-pad                 | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)               |
| A                     | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               |
| Turbo A               | ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               |
| L                     | ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   |
| R                     | ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   |
| Turbo L               | ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              |
| Turbo R               | ![RetroPad_R2](images/RetroPad/Retro_R2.png)                   |
| Darken Solar Sensor   | ![RetroPad_L3](images/RetroPad/Retro_L3.png)                   |
| Brighten Solar Sensor | ![RetroPad_R3](images/RetroPad/Retro_R3.png)                   |
|                       | ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)   |
|                       | ![RetroPad_Right_Stick](images/RetroPad/Retro_Right_Stick.png) |

## Compatibility

Please file bugs that are reproducible on upstream standalone on the [bug tracker](https://endrift.com/mgba/bugs/).

## External Links

* [Libretro Repository](https://github.com/libretro/mgba)
* [Report Core Issues Here](https://github.com/libretro/libretro-meta/issues)
* [Official Website](https://mgba.io/)
* [Official GitHub Repository](https://github.com/mgba-emu/mgba)
