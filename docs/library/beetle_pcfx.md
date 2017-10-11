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

| Feature           | Supported |
|-------------------|:---------:|
| Saves             | ✔         |
| States            | ✔         |
| Rewind            | ✔         |
| Netplay           | ✔         |
| RetroAchievements | ✕         |
| RetroArch Cheats  | ✕         |
| Native Cheats     | ✕         |
| Controllers       | ✔         |
| Rumble            | ✕         |
| Sensors           | ✕         |
| Camera            | ✕         |
| Location          | ✕         |
| Subsystem         | ✕         |

## Options

The (Beetle PC-FX) core has the following options that can be tweaked from the core options menu. The default setting is bolded.

- **High Dotclock Width (Restart)** (**1024**/256/341): Emulated width for 7.16MHz dot-clock mode. Lower values are faster, but will cause some degree of pixel distortion.
- **Suppress Channel Reset Clicks (Restart)** (**On**/Off): Hack to suppress clicks caused by forced channel resets.
- **Emulate Buggy Codec (Restart)** (**Off**/On): 	Hack that emulates the codec a buggy ADPCM encoder used for some games' ADPCM..
- **Sound Quality (Restart)** (**3**/1-5): Higher values correspond to better SNR and better preservation of higher frequencies("brightness"), at the cost of increased computational complexity and a negligible increase in latency.
- **Chroma channel bilinear interpolation (Restart)** (**Off**/On): Enable bilinear interpolation on the chroma channel of RAINBOW YUV output. Enabling it may cause graphical glitches with some games.
- **No Sprite Limit (Restart)** (**Off**/On): Remove 16-sprites-per-scanline hardware limit. 
- **Initial Scanline** (**4**/0-40): Set initial rendered scanline position.
- **Last Scanline** (208-**235**-239): Set last rendered scanline position.

## Controllers

The (Beetle PC-FX) core supports 2 controller setting(s):

* PC-FX Controller

* PC-FX Mouse

| Beetle PC-FX | [RetroPad](RetroPad)                                        |
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
