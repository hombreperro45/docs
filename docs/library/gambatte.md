# Game Boy / Game Boy Color (Gambatte)

## Background

Gambatte is an accuracy-focused, open-source, cross-platform Game Boy Color emulator written in C++. It is based on hundreds of corner case hardware tests, as well as previous documentation and reverse engineering efforts.

Author(s): Sinamas

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/gambatte.md). Changes are proposed using "Pull Requests."

## License

GPLv2

## Extensions

gb|gbc|dmg

## BIOS

Gambatte does not support using BIOS image files.

## Feature Support
These are libretro features, not frontend or standalone emulator features.

##### Features:

| Saves | States      | Rewind | Netplay | RetroAchievements | Cheats |
|:-----:|:-----------:|:------:|:-------:|:-----------------:|:------:|
|  yes  |     yes     |   yes  |   no    |        -          | yes    |

| Controllers     | Rumble | Sensors | Camera | Location | Subsystem     |
|:---------------:|:------:|:-------:|:------:|:--------:|:-------------:|
|       no        |  no    |   no    |  no    |   no     |      no       |

## Options

This core has a few options that can be tweaked from the core options menu. The default setting is bolded:

- **GB Colorization** (**disabled**/auto/internal/custom): Colorizes Game Boy games.
- **Internal Palette** (**GBC - Blue**/GBC - Brown/GBC - Dark Blue/GBC - Dark Brown/GBC - Dark Green/GBC - Grayscale/GBC - Green/GBC - Inverted/GBC - Orange/GBC - Pastel Mix/GBC - Red/GBC - Yellow/Special 1/Special 2/Special 3): Select which internal color palette is going to be used.
- **Color Correction** (**enabled**/disabled): Darkens Game Boy Color games to match the original hardware output.
- **gambatte_gb_hwmode** (Auto/GB/GBA): Forces Gambatte to boot into a specific hardware mode.
- **Emulated Hardware (restart):** (**Auto**/GB/GBC/GBA): Choose which hardware is emulated Game Boy, Game Boy Color, or Game Boy Advance
- **Use official bootloader:** (**enabled**/disabled)
- **Gameboy Link Mode:** (**Not Connected**/Network Server/Network Client)
- **Network Link Port:** (**56400**)
- **Network link server add:** (**0**)
- **Network link server add:** (**0**)
- **Network link server add:** (**0**)
- **Network link server add:** (**0**)

## Controllers

![Game Boy Diagram](images/Controllers/Game-Boy_joypad.png)

The core supports controller setting:

* Gambatte Joypad: Game Boy Controller

| [RetroPad](RetroPad)                                           | Joypad |
|----------------------------------------------------------------|--------|
| ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               |A button (right)|
| ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               |B button (down)|
| ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)               |dpad        |
| ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   |        |
| ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              |        |
| ![RetroPad_L3](images/RetroPad/Retro_L3.png)                   |        |
| ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)   |        |
| ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   |        |
| ![RetroPad_R2](images/RetroPad/Retro_R2.png)                   |        |
| ![RetroPad_R3](images/RetroPad/Retro_R3.png)                   |        |
| ![RetroPad_Right_Stick](images/RetroPad/Retro_Right_Stick.png) |        |
| ![RetroPad_Select](images/RetroPad/Retro_Select.png)           |Select        |
| ![RetroPad_Start](images/RetroPad/Retro_Start.png)             |Start        |
| ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               |        |
| ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               |        |

## Compatibility

| Game                                  | Issue                          |
|---------------------------------------|--------------------------------|
|**Command Master**                     |Crashes on start. Unemulated MBC7 mapper. |
|**Game Boy Camera**|Crashes on start. Unemulated Pocket Camera mapper. |
|**Game de Hakken!! Tamagotchi - Osutchi to Mesutchi** |Crashes on start. Unemulated TAMA5 mapper. |
|**Kirby Tilt 'n' Tumble** |Crashes on start. Unemulated MBC7 mapper. |
|**Net de Get: Mini-Game @ 100**| 	Crashes on start. Unemulated MBC6 mapper. |
|**Pocket Family GB2**|Crashes on start. Unemulated HuC3 mapper. |
|**Robopon: Sun/Star/Moon Version**|Crashes on start. Unemulated HuC3 mapper. |

## External Links

* [Official Website](https://sourceforge.net/projects/gambatte/)  
* [Libretro Repository](https://github.com/libretro/gambatte-libretro)
* [Report Issues Here](https://github.com/libretro/libretro-meta)
