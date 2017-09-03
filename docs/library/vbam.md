# Game Boy Advance (VBA-M)

## Background

VBA-M is a Game Boy Advance emulator with the goal to improve upon VisualBoyAdvance by integrating the best features from the various builds floating around.

Author(s): Forgotten|VBA-M Team

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/vbam.md). Changes are proposed using "Pull Requests."

## License

GPLv2

## Extensions

gba

## BIOS

The VBA-M core does not feature BIOS use.

## Features

| Saves | States      | Rewind | Netplay | RetroAchievements | RetroArch Cheats | Native Cheats |
|:-----:|:-----------:|:------:|:-------:|:-----------------:|:----------------:|:-------------:|
| yes   |   yes       | yes    |  no     |        -          | yes              | -             |

| Controllers     | Rumble | Sensors | Camera | Location | Subsystem     |
|:---------------:|:------:|:-------:|:------:|:--------:|:-------------:|
|       no        |  no    |   no    |  no    |   no     |      no       |

## Options

The VBA-M core has the following options that can be tweaked from the core options menu. The default setting is bolded.

- **Show layer 1** (**Yes**/On): -
- **Show layer 2** (**Yes**/On): -
- **Show layer 3** (**Yes**/On): -
- **Show layer 4** (**Yes**/On): - 
- **Show sprite layer** (**Yes**/On): -
- **Show window layer 1** (**Yes**/On): - 
- **Show window layer 2** (**Yes**/On): -
- **Show sprite window layer** (**Yes**/On): - 

## Controllers

The VBA-M core supports four controller setting(s):

* RetroPad

![vbam_retropad](images/Controllers/vbam_retropad.png)

* GBA Joypad

![vbam_gbajoypad](images/Controllers/vbam_gbajoypad.png)

* Alt Joypad YB

![vbam_altjoypadyb](images/Controllers/vbam_altjoypadyb.png)

* Alt Joypad AB

![vbam_altjoypadab](images/Controllers/vbam_altjoypadab.png)

| VBA-M     | [RetroPad](RetroPad)                                           | GBA Joypad | Alt Joypad YB | Alt Joypad AB |
|-----------|----------------------------------------------------------------|------------|---------------|---------------|
| B         | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               | -          | -             | -             |
|           | ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               |            |               |               |
| Select    | ![RetroPad_Select](images/RetroPad/Retro_Select.png)           | -          | -             | -             |
| Start     | ![RetroPad_Start](images/RetroPad/Retro_Start.png)             | -          | -             | -             |
| D-pad     | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)               | -          | -             | -             |
| A         | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               | -          | -             | -             |
|           | ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               |            |               |               |
| L         | ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   | -          | -             | -             |
| R         | ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   | -          | -             |               |
|           | ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              |            |               |               |
|           | ![RetroPad_R2](images/RetroPad/Retro_R2.png)                   |            |               |               |
|           | ![RetroPad_L3](images/RetroPad/Retro_L3.png)                   |            |               |               |
|           | ![RetroPad_R3](images/RetroPad/Retro_R3.png)                   |            |               |               |
|           | ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)   |            |               |               |
|           | ![RetroPad_Right_Stick](images/RetroPad/Retro_Right_Stick.png) |            |               |               |


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

* [Libretro Repository](https://github.com/libretro/vbam-libretro)
* [Report Libretro Issues Here](https://github.com/libretro/libretro-meta/issues)
* [Official Website](http://vba-m.com/)
* [Official Sourceforge Repository](http://sourceforge.net/projects/vbam/)
