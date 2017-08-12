# Game Boy Advance (VBA-M)

## Background

VBA-M is a Game Boy Advance emulator with the goal to improve upon VisualBoyAdvance by integrating the best features from the various builds floating around.
## License

GPLv2

## Extensions

gba

## BIOS

The libretro port of VBA-M does not support using BIOS image files.

## Feature Support
These are libretro features, not frontend or standalone emulator features.

##### Features:

| Saves | States      | Rewind | Netplay | RetroAchievements | Cheats |
|:-----:|:-----------:|:------:|:-------:|:-----------------:|:------:|
| yes   |   yes       | yes    |  no     |        -          | yes    |

| Controllers     | Rumble | Sensors | Camera | Location | Subsystem     |
|:---------------:|:------:|:-------:|:------:|:--------:|:-------------:|
|       no        |  no    |   no    |  no    |   no     |      no       |

## Options

|   Core Option   |         Description        | Options (Default Bolded) | Requires Restart |
|:---------------:|:--------------------------:|:------------------------:|:-----------:|
|Show Layer 1     | -                          |   **Yes**/On             |   -         |
|Show Layer 2     | -                          |   **Yes**/On             |   -         |
|Show Layer 3     | -                          |   **Yes**/On             |   -         |
|Show Layer 4     | -                          |   **Yes**/On             |   -         |
|Show sprite layer| -                          |   **Yes**/On             |   -         |
|Show window layer 1| -                        |   **Yes**/On             |   -         |
|Show window layer 2| -                        |   **Yes**/On             |   -         |
|Show sprite window layer| -                   |   **Yes**/On             |   -         |

## Controllers

The VBA-M core supports one controller setting:

* Joypad: Controller

![Game Boy Advance_joypad_diagram](images/Controllers/Game-Boy-Advance_joypad.png)

| [RetroPad](RetroPad)                                           | Joypad |
|----------------------------------------------------------------|--------|
| ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               |    A   |
| ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               |    B   |
| ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)               | D-Pad  |
| ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   |Left Shoulder  |
| ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              |        |
| ![RetroPad_L3](images/RetroPad/Retro_L3.png)                   |        |
| ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)   |        |
| ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   |Right Shoulder |
| ![RetroPad_R2](images/RetroPad/Retro_R2.png)                   |        |
| ![RetroPad_R3](images/RetroPad/Retro_R3.png)                   |        |
| ![RetroPad_Right_Stick](images/RetroPad/Retro_Right_Stick.png) |        |
| ![RetroPad_Select](images/RetroPad/Retro_Select.png)           | Select |
| ![RetroPad_Start](images/RetroPad/Retro_Start.png)             | Start  |
| ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               |        |
| ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               |        |

## Compatibility

| Game                                  | Issue                          |
|---------------------------------------|--------------------------------|
|**Boktai Trilogy**                     | The solar sensor is not emulated|
|**Digimon Racing (Europe)**            |Freezes during the intro. This can be avoided by enabling linking in the standalone VBA-M release  |
|**Koro Koro Puzzle Happy Panechu!**    |	The tilt sensor is not emulated|
|**Phantasy Star Collection**           | Digital Eclipse logo sound effect is missing. Phantasy Star 1 flickers |
|**WarioWare: Twisted!**                |  	The tilt sensor is not emulated   |
|**Yoshi’s Universal Gravitation**      |   The tilt sensor is not emulated   |


## External Links

* [Official Website](http://vba-m.com/)
* [Official Sourceforge Repository](http://sourceforge.net/projects/vbam/)
* [Libretro Repository](https://github.com/libretro/vbam-libretro)
