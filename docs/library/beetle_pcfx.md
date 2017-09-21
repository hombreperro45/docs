# PC-FX (Beetle PC-FX)

## Background

Beetle PC-FX is a port of Mednafen PC-FX video game system emulator for the NEC PC-FX.

Author(s): Mednafen Team

## Contribute to this documentation

+In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/beetle_pcfx.md). Changes are proposed using "Pull Requests."


## License

GPLv2

## Extensions

cue|ccd|toc

## BIOS

|   Filename    |    Description              |              md5sum              |
|:-------------:|:---------------------------:|:--------------------------------:|
|   pcfx.rom    |PC-FX BIOS v1.00 - 2 Sep 1994| 08e36edbea28a017f79f8d4f7ff9b6d7 |


## Features

| Saves | States      | Rewind | Netplay | RetroAchievements | RetroArch Cheats | Native Cheats |
|:-----:|:-----------:|:------:|:-------:|:-----------------:|:----------------:|:-------------:|
| Yes   |    Yes      |  Yes   |  Yes    |        -          |   No             | -             |

| Controllers     | Multi Mouse | Rumble | Sensors | Camera | Location | Subsystem     |
|:---------------:|:-----------:|:------:|:-------:|:------:|:--------:|:-------------:|
|      Yes        |      -      |   No   |   No    |   No   |   No     |     No        |

## Options

The (Beetle PC-FX) core has the following options that can be tweaked from the core options menu. The default setting is bolded.

- **High Dotclock Width** (**1024**/256/341): Description. **Restart**
- **Suppress Channel Reset Clicks** (**On**/Off): Description. **Restart**
- **Emulate Buggy Codec** (**Off**/On): Description. **Restart**
- **Sound Quality** (**3**/1-5): Description. **Restart**
- **Chroma channel bilinear interpolation** (**Off**/On): Description. **Restart**
- **No Sprite Limit** (**Off**/On): Description. **Restart**
- **Initial Scanline** (**4**/0-40): Set initial scanline position.
- **Last Scanline** (**235**/208-239): Set last scanline position.

## Controllers

The (Beetle PC-FX) core supports 2 controller setting(s):

* PC-FX Controller
* PC-FX Mouse

* RetroPad

![retropad](images/controllers/retropad.png)

| Core Name | [RetroPad](RetroPad)                                           |
|-----------|----------------------------------------------------------------|
|    II     | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               |
|    IV     | ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               |
|  Select   | ![RetroPad_Select](images/RetroPad/Retro_Select.png)           |
|   Start   | ![RetroPad_Start](images/RetroPad/Retro_Start.png)             |
|  D-Pad    | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)               |
|    I      | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               |
|   III     | ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               |
|    V      | ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   |
|    VI     | ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   |
|  MODE 1   | ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              |
|  MODE 2   | ![RetroPad_R2](images/RetroPad/Retro_R2.png)                   |

## Compatibility

| Game                                                                    | Issue                                           |
|-------------------------------------------------------------------------|-------------------------------------------------|
| **Pia Carrot e Youkoso!! (Japan) [T-En by David Michel + filler v1.0]** |Doesn't boot. Confirmed to work on real hardware.|


## External Links

* [Libretro Repository](https://github.com/libretro/beetle-pcfx-libretro)
* [Report Core Issues Here](https://github.com/libretro/libretro-meta)
* [Official Website](https://mednafen.github.io/)
* [Official Upstream Downloads](https://mednafen.github.io/releases/)
