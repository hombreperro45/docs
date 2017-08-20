# Game Boy Advance (VBA Next)

## Background

VBA-Next is a Game Boy Advance emulator based on [VBA-M](https://wiki.libretro.com/index.php?title=VBA-M) 2011 with backported patches for performance and compatibility improvements.

Author(s): Forgotten|VBA-M Team|Squarepusher

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/vba_next.md). Changes are proposed using "Pull Requests."

## License

GPLv2

## Extensions

gba

## BIOS

|   Filename    |    Description        |              md5sum              |
|:-------------:|:---------------------:|:--------------------------------:|
|gba_bios.bin   |Game Boy Advance Image - Required | a860e8c0b6d573d191e4ec7db1b1e4f6 |

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

The VBA-Next core has the following options that can be tweaked from the core options menu. The default setting is bolded.

- **Use Bios (if available)** (**On**/Off): Will use an available Bios

## Controllers

The VBA-Next core supports one controller setting(s):

* RetroPad

![vba_next_retropad](images/Controllers/vba_next_retropad.png)

| VBA-Next  | [RetroPad](RetroPad)                                           |
|-----------|----------------------------------------------------------------|
| B         | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               |
|           | ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               |
| Select    | ![RetroPad_Select](images/RetroPad/Retro_Select.png)           |
| Start     | ![RetroPad_Start](images/RetroPad/Retro_Start.png)             |
| D-pad     | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)               |    
| A         | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               |
|           | ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               |
| L         | ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   |
| R         | ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   |
|           | ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              |
|           | ![RetroPad_R2](images/RetroPad/Retro_R2.png)                   |
|           | ![RetroPad_L3](images/RetroPad/Retro_L3.png)                   |
|           | ![RetroPad_R3](images/RetroPad/Retro_R3.png)                   |
|           | ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)   |
|           | ![RetroPad_Right_Stick](images/RetroPad/Retro_Right_Stick.png) |

## Compatibility

| Game                                  | Issue                          |
|---------------------------------------|--------------------------------|
|**Advanced Dungeons & Dragons - Deathkeep**| Random softlocks (music related?). |
|**Alone in the Dark**|Unreadable text within books. Audio glitches. |
|**DinoPark Tycoon**| 	Graphics glitches. |
|**Eye of Typhoon, The**| 	Runs too fast. |
|**Horde, The**| 	Graphics glitches. Minor graphical inaccuracy in bird's eye map. |
|**Primal Rage**|Primal Rage|
|**Psychic Detective**|Psychic Detective|
|**Psychic Detective**|Psychic Detective|
|**Tetsujin Return**| 	Graphics glitches. Missing graphics for obstacles in the driving scenes. |

## External Links

* [Libretro Repository](https://github.com/libretro/vba-next)
* [Report Libretro Issues Here](https://github.com/libretro/libretro-meta/issues)
