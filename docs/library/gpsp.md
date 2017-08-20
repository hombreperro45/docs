# Game Boy Advance (gpSP)

## Background

gpSP is a Game Boy Advance emulator based on notaz' fork of gpSP with additional codebase improvements.

Author(s): Exophase

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/blob/master/docs/library/gpsp.md). Changes are proposed using "Pull Requests."

## License

GPLv2

## Extensions

gba|bin

## BIOS

|   Filename    |    Description        |              md5sum              |
|:-------------:|:---------------------:|:--------------------------------:|
|gba_bios.bin   |Game Boy Advance Image | a860e8c0b6d573d191e4ec7db1b1e4f6 |

## Feature Support

These are libretro features, not frontend or standalone emulator features.

##### Features:

| Saves | States      | Rewind | Netplay | RetroAchievements | Cheats |
|:-----:|:-----------:|:------:|:-------:|:-----------------:|:------:|
|  yes  |   yes       |  yes   |  no     |        -          |  no    |

| Controllers     | Rumble | Sensors | Camera | Location | Subsystem     |
|:---------------:|:------:|:-------:|:------:|:--------:|:-------------:|
|       no        |  no    |   no    |  no    |   no     |      no       |

## Options

This core does not feature core options.

## Controllers

The core supports one controller setting:

* Joypad: Controller

![Game Boy Advance_joypad_diagram](images/Controllers/Game-Boy-Advance_joypad.png)

Note: Shoulder buttons are not supported

| [RetroPad](RetroPad)                                           | Joypad |
|----------------------------------------------------------------|--------|
| ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               |    A   |
| ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               |    B   |
| ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)               | D-Pad  |
| ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   |        |
| ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              |        |
| ![RetroPad_L3](images/RetroPad/Retro_L3.png)                   |        |
| ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)   |        |
| ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   |        |
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
|**Activision Anthology**               |Freezes when entering a game. |
|**Banjo-Kazooie - Grunty's Revenge**   |Black screen during developer logo. Resets when Banjo leaves his house.|
|**Boktai Trilogy**                     |The solar sensor is not emulated. |
|**DemiKids - Light/Dark Version**      |Crashes when entering a battle. |
|**Digimon Racing (Europe)**            |Freezes during the intro.   |
|**Dragon Ball Z - The Legacy of Goku** |Graphics glitches. See [Image](images/Compatibility/gpsp_DBZ-Legacy_of_Goku.png)     |
|**Final Fantasy VI**                   |Background/tiling order issues.  |
|**Game Boy Advance Video - Dragon Ball GT - Volume 1**|White screen.     |
|**Grand Theft Auto Advance**           |Crashes after first dialog.      |
|**Harry Potter - Quidditch World Cup** |Crashes when going ingame.       |
|**Koro Koro Puzzle Happy Panechu!**    |The tilt sensor is not emulated. |
|**Mario & Luigi - Superstar Saga**     |Crashes when entering a battle.  |
|**Phantasy Star Collection**           |Phantasy Star 1 flickers.        |
|**R-Type III - The Third Lightning**   |Softlocks at Irem startup screen.|
|**Rock 'n Roll Racing**                |Corrupted graphics, not playable.|
|**Rockman & Forte**                    |Doesn't continue after GBA BIOS screen.|
|**Sims 2, The - Pets**|Graphics glitches. Heavy flickering, black objects. See [Image](images/Compatibility/gpsp_The_Sims2_Pets.png)|
|**Street Racing Syndicate**            |Freezes at startup screen, doesn't continue.|
|**Super Monkey Ball Jr.**              |Softlocks at startup screen.|
|**Super Street Fighter II Turbo/X Revival**|Small graphics glitch. Selecting speed 'Turbo 1' and beyond on the character select screen makes the game speed window not fully visible. See [Image](images/Compatibility/gpsp_SSF2_TurboX_Revival.png)|
|**Tales of Phantasia (USA version)**   |Softlocks during the introduction sequence (just before the small guy hits the tall guy in the right).|
|**WarioWare: Twisted!**                |The tilt sensor is not emulated.|
|**Wolfenstein 3D**                     |Softlocks at id Software startup screen.|
|**Yoshi’s Universal Gravitation**      |The tilt sensor is not emulated.|

## External Links

* [Libretro Repository](https://github.com/libretro/gpsp)
* [Report Issues Here](https://github.com/libretro/libretro-meta/issues)
