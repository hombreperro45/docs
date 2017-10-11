# PC Engine/PCE-CD (Beetle PCE FAST)

## Background

Beetle/Mednafen PCE FAST is a libretro port of Mednafen PCE Fast with the PC Engine SuperGrafx module removed. It is a video game system emulator for TurboGrafx-16/NEC PC Engine/CD

Author(s): Mednafen Team

## Contribute to this documentation

+In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/beetle_pce_fast.md). Changes are proposed using "Pull Requests."


## License

GPLv2

## Extensions

pce|cue|ccd|iso|img|bin|chd

## BIOS

|   Filename    |    Description     |              md5sum              |
|:-------------:|:------------------:|:--------------------------------:|
| syscard3.pce  |     PCE-CD BIOS - Required    | 38179df8f4ac870017db21ebcbf53114 |
| syscard1.pce  |     PCE-CD BIOS - Optional    |                                  |
| syscard2.pce  |     PCE-CD BIOS - Optional    |                                  |
| gexpress.pce  |     PCE-CD BIOS - Optional    |                                  |

!!! note
    Any CD-ROM System BIOS will work, but some them are known to be incompatible with certain games.

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

The (Beetle PCE Fast) core has the following options that can be tweaked from the core options menu. The default setting is bolded.

- **CD Image Cache (Restart)** (**On**/Off): Caches the entire CD image. Can potentially decrease loading times at the cost of increased startup time.
- **CD Bios (Restart)** (**System Card 3**/System Card 2/System Card 1/Game Express): Select required BIOS
- **No Sprite Limit (Restart)** (**Off**/On): Disables the sprite limit.
- **CPU Overclock Multiplier (Restart)** (**1**/1-50): Description.
- **Horizontal Overscan (352 Width Mode Only)** (**352**/300-352): Description.
- **Initial scanline** (**3**/0-40): Position of the rendered initial scanline.
- **Last scanline** (**242**/208-242): Position of the rendered last scanline.
- **(CD) CDDA Volume %** (**100**/0-200): Volume of the CDDA.
- **(CD) ADPCM Volume %** (**100**/0-200): Volume of the ADPCM.
- **(CD) PSG Volume %** (**100**/0-200): Volume of the CD PSG.
- **(CD) CD Speed** (**1**/2/4/8): Set the speed of the emulated CD drive.
- **Turbo Delay** (**Fast**/Medium/Slow): Description.
- **P# Turbo I** (**Off**/On): Description.
- **P# Turbo II** (**Off**/On): Description.

## Controllers

The (Beetle PCE Fast) core supports 2 controller setting(s):

* PCE Joypad
* Mouse

![retropad](images/controllers/retropad.png)

| Core Name | [RetroPad](RetroPad)                                           |
|-----------|----------------------------------------------------------------|
| II        | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               |
| III       | ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               |
| Select    | ![RetroPad_Select](images/RetroPad/Retro_Select.png)           |
| Run       | ![RetroPad_Start](images/RetroPad/Retro_Start.png)             |
| D-pad     | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)               |
| I         | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               |
| IV        | ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               |
| V         | ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   |
| VI        | ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   |
|Mode Switch| ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              |

## Compatibility

Unknown

## External Links

* [Libretro Repository](https://github.com/libretro/beetle-pce-fast-libretro)
* [Report Core Issues Here](https://github.com/libretro/libretro-meta)
* [Official Website](http://mednafen.sourceforge.net/)
* [Official Upstream Downloads](https://mednafen.github.io/releases/)
