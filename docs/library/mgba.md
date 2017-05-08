# Game Boy Advance (mGBA)

![Game Boy Advance_banner](images/Banners/Game-Boy-Advance_banner.png)

## Background
mGBA is a new emulator for running Game Boy Advance games. It aims to be faster and more accurate than many existing Game Boy Advance emulators, as well as adding features that other emulators lack.
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
| Saves | Save | states | Rewind | Netplay | RetroAchievements | Cheats | Controllers |
|-------|------|--------|--------|---------|-------------------|--------|-------------|
| yes   |   -  |   yes  |  yes   |   no    |         -         |   no   |      no     |

| Rumble | Sensors | Camera | Location | Subsystem |
|--------|---------|--------|----------|-----------|
|    no  |   no    |   no   |    no    |    no     |

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
![Game Boy Advance_joypad_diagram]()

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

Please file bugs on the [bug tracker](https://endrift.com/mgba/bugs/) instead of having some secondary source of "bugs".

## External Links

* [Official Website](http://mgba.io/)
* [Official GitHub Repository](https://github.com/mgba-emu/mgba)
* [Libretro Repository](https://github.com/libretro/mgba)
