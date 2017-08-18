# Game Boy Advance (VBA Next)

## Background

VBA-Next is a Game Boy Advance emulator based on [VBA-M](https://wiki.libretro.com/index.php?title=VBA-M) 2011 with backported patches for performance and compatibility improvements.

Author(s):

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/vba_next.md). Changes are proposed using "Pull Requests."

## License

GPLv2

## Extensions

gba

## BIOS

|   Filename    |    Description        |              md5sum              |
|:-------------:|:---------------------:|:--------------------------------:|
|gba_bios.bin   |Game Boy Advance Image | a860e8c0b6d573d191e4ec7db1b1e4f6 |

## Feature Support

These are libretro features, not frontend or standalone emulator features.

##### Features:

| Saves | States      | Rewind | Netplay | RetroAchievements | Cheats |
|:-----:|:-----------:|:------:|:-------:|:-----------------:|:------:|
|  yes  |    yes      | yes    |  no     |        -          | yes    |

| Controllers     | Rumble | Sensors | Camera | Location | Subsystem     |
|:---------------:|:------:|:-------:|:------:|:--------:|:-------------:|
|       no        | no     |   no    |  no    |   no     |      no       |

## Options

|   Core Option   |         Description        | Options (Default Bolded) | Requires Restart |
|:---------------:|:--------------------------:|:------------------------:|:-----------:|
| Use Bios        | Will use an available Bios |   **On**/Off             |   Yes       |


## Controllers

The VBA Next core supports one controller setting:

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
|**Croket! 2 – Yami no Bank to Banqueen**|Heavy slowdown when approaching the snowman in the beginning|
|**Digimon Racing (Europe)**            |Freezes during the intro. This can be avoided by enabling linking in the standalone VBA-M release  |
|**Drome Racers**                       |Only shows a black screen after the THQ logo|
|**Hamtaro: Ham-Ham Games**             |Locks up if the opening cinematics aren’t skipped|
|**Hot Wheels - Stunt Track Challenge** |Resets itself when trying to go in-game|
|**Jurassic Park III: Park Builder**    |  	Unreadable glitched text     |
|**Koro Koro Puzzle Happy Panechu!**    |	The tilt sensor is not emulated|
|**Moto GP**                            | Black screen, loud screeching noise|
|**Phantasy Star Collection**           | Digital Eclipse logo sound effect is missing. Phantasy Star 1 flickers |
|**SSX 3**                              |  	Graphics glitches. Seems pitch-related. See [Image](images/Compatibility/VBA-Next_SSX-3.png)  |
|**Super Mario Advance 2: Super Mario World (Europe)** |The program crashes during the final fight, when Bowser approaches (zoom mode 7)  |
|**WarioWare: Twisted!**                |  	The tilt sensor is not emulated   |
|**Yoshi’s Universal Gravitation**      |   The tilt sensor is not emulated   |


## External Links

* [Libretro Repository](https://github.com/libretro/vba-next)
