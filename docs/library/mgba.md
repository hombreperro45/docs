# Game Boy Advance (mGBA)

## Background

mGBA is a new emulator for running Game Boy Advance games. It aims to be faster and more accurate than many existing Game Boy Advance emulators, as well as adding features that other emulators lack.

Author(s): Vicki Pfau

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/mgba.md). Changes are proposed using "Pull Requests."


## License

MPLv2.0

## Extensions

gb|gbc|gba

## BIOS

mGBA optionally supports using the following BIOS image file for operation:

|   Filename    |    Description       |              md5sum              |
|:-------------:|:--------------------:|:--------------------------------:|
|gba_bios.bin   |Game Boy Advance BIOS | a860e8c0b6d573d191e4ec7db1b1e4f6 |

## Feature Support

These are libretro features, not frontend or standalone emulator features.

##### Features:

| Saves | States      | Rewind | Netplay | RetroAchievements | Cheats |
|:-----:|:-----------:|:------:|:-------:|:-----------------:|:------:|
|  yes  |   yes       | yes    |  no     |        -          |   no   |

| Controllers     | Rumble | Sensors | Camera | Location | Subsystem     |
|:---------------:|:------:|:-------:|:------:|:--------:|:-------------:|
|       no        |  no    |   no    |  no    |   no     |      no       |

## Options

|   Core Option   |         Description        | Options (Default Bolded) | Requires Restart |
|:---------------:|:--------------------------:|:------------------------:|:-----------:|
|Solar sensor level | -                        |   **0**-10               |   -         |
|Allow opposing directional input| -           |   **Off**/On             |   -         |
|Use BIOS file if found| -                     |   **On**/Off             |   -         |
|Skip BIOS intro| -                            |   **Off**/On             |   -         |
|Idle loop removal| -     |**Remove Known**/Detect and Remove/Don't Remove|   -         |

## Controllers

The mGBA core supports one controller setting:

* Joypad: Controller

![Game Boy Advance_joypad_diagram](images/Controllers/Game-Boy-Advance_joypad.png)

Note: This core supports additional buttons for:-
Turbo L (L2)
Darken Solar Sensor (L3)
Turbo R (R2)
Brighten Solar Sensor (R3)
Turbo A (X)
Turbo B (Y)

| [RetroPad](RetroPad)                                           | Joypad |
|----------------------------------------------------------------|--------|
| ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               |    A   |
| ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               |    B   |
| ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)               | D-Pad  |
| ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   |Left Shoulder  |
| ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              |Turbo L |
| ![RetroPad_L3](images/RetroPad/Retro_L3.png)                   |Darken Solar Sensor|
| ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)   |        |
| ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   |Right Shoulder |
| ![RetroPad_R2](images/RetroPad/Retro_R2.png)                   |Turbo R |
| ![RetroPad_R3](images/RetroPad/Retro_R3.png)                   |Brighten Solar Sensor|
| ![RetroPad_Right_Stick](images/RetroPad/Retro_Right_Stick.png) |        |
| ![RetroPad_Select](images/RetroPad/Retro_Select.png)           | Select |
| ![RetroPad_Start](images/RetroPad/Retro_Start.png)             | Start  |
| ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               |Turbo A |
| ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               |Turbo B |

## Compatibility

Please file bugs on the [bug tracker](https://endrift.com/mgba/bugs/).

## External Links

* [Libretro Repository](https://github.com/libretro/mgba)
* [Report Issues Here](https://github.com/libretro/libretro-meta/issues)
* [Official Website](http://mgba.io/)
* [Official GitHub Repository](https://github.com/mgba-emu/mgba)
