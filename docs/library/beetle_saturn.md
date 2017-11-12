# Sega Saturn (Beetle Saturn)

## Background

Port of standalone Mednafen Saturn to libretro

Author(s): Mednafen Team

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/beetle_saturn.md). Changes are proposed using "Pull Requests."

## See also

[Yabause](https://buildbot.libretro.com/docs/library/Yabause/)

## License

GPLv2

## Extensions

cue|toc|m3u|ccd|chd

## BIOS

Required or optional firmware files go in RetroArch's system directory.

|   Filename       |    Description                                                             |              md5sum              |
|:----------------:|:--------------------------------------------------------------------------:|:--------------------------------:|
| sega_101.bin     | Saturn JP BIOS - Required                                                  | 85ec9ca47d8f6807718151cbcca8b964 |
| mpr-17933.bin    | Saturn US/EU BIOS - Required                                               | 3240872c70984b6cbfda1586cab68dbe |
| mpr-18811-mx.ic1 | The King of Fighters '95 ROM Cartridge - Required for this game            | 255113ba943c92a54facd25a10fd780c |
| mpr-19367-mx.ic1 | Ultraman: Hikari no Kyojin Densetsu ROM Cartridge - Required for this game | 1cd19988d1d72a3e7caa0b73234c96b4 |

## Features

| Feature           | Supported |
|-------------------|:---------:|
| Saves             | ✔         |
| States            | ✔         |
| Rewind            | ✕         |
| Netplay           | ✕         |
| RetroAchievements | ✕         |
| RetroArch Cheats  | ✕         |
| Native Cheats     | ✕         |
| Controllers       | ✔         |
| Multi-Mouse       | ✕         |
| Rumble            | ✕         |
| Sensors           | ✕         |
| Camera            | ✕         |
| Location          | ✕         |
| Subsystem         | ✕         |

The Beetle Saturn core creates directories named Mednafen Saturn in RetroArch's save and state directories 

Game data is saved/loaded to and from the core's save directory  

## Options

The Beetle Saturn core has the following options that can be tweaked from the core options menu. The default setting is bolded.

- **CD Image Cache (restart)** (**Off**/On): Loads the complete image in memory at startup.
- **Automatically set RTC on game load** (Off/**On**): Automatically set the SMPC's emulated Real-Time Clock to the host system's current time and date upon game load.
- **BIOS language** (**english**/german/french/spanish/italian/japanese): Self explanatory. Also affects language used in some games (e.g. the European release of "Panzer Dragoon"). 
- **Initial scanline** (**0**-40): First displayed scanline in NTSC mode.
- **Initial scanline PAL** (**0**-40): First displayed scanline in PAL mode.
- **Last scanline** (210-**239**): Last displayed scanline in NTSC mode.
- **Last scanline PAL** (260-**287**): Last displayed scanline in PAL mode.
- **Analog Deadzone (percent)** (0/5/10/**15**/20/25/30): Deadzone adjustment for the 3D Pad device type's analog stick.

## Controllers

The Beetle Saturn core supports 3 controller setting(s), the bolded controller setting is default:

* **[Saturn Joypad](http://segaretro.org/Control_Pad_(Saturn))** - [Joypad]

* [3D Pad](http://segaretro.org/3D_Control_Pad) - [Analog] - To avoid compatibility issues, the 3D Pad has a switch to swap between "Digital" and "Analogue" modes. Switching to "Digital" mode disables all analog settings, essentially turning the controller back into a standard Saturn Joypad.

* [Mouse](http://segaretro.org/Shuttle_Mouse) - [Mouse] - *Currently doesn't work in this libretro core*

| Beetle Saturn             | RetroPad                                                       | **Saturn Joypad** | 3D Pad               |
|---------------------------|----------------------------------------------------------------|-------------------|----------------------|
| A                         | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               | A                 | A                    |
| X                         | ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               | X                 | X                    |
| (3D Pad) Mode Switch      | ![RetroPad_Select](images/RetroPad/Retro_Select.png)           |                   | (3D Pad) Mode Switch |
| Start                     | ![RetroPad_Start](images/RetroPad/Retro_Start.png)             | Start             | Start                |
| D-Pad Up                  | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Up.png)            | D-Pad Up          | D-Pad Up             |
| D-Pad Down                | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Down.png)          | D-Pad Down        | D-Pad Down           |
| D-Pad Left                | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Left.png)          | D-Pad Left        | D-Pad Left           |
| D-Pad Right               | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Right.png)         | D-Pad Right       | D-Pad Right          |
| B                         | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               | B                 | B                    |
| Y                         | ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               | Y                 | Y                    |
| C                         | ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   | C                 | C                    |
| Z                         | ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   | Z                 | Z                    | 
| L                         | ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              | L                 | L                    |
| R                         | ![RetroPad_R2](images/RetroPad/Retro_R2.png)                   | R                 | R                    |
| Analog                    | ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)   |                   | Analog               |

| RetroMouse                                                      | Mouse         | 
|-----------------------------------------------------------------|---------------|
| ![Retro_Mouse](images/RetroMouse/Retro_Mouse.png)               | Pointer       | 
| ![RetroP_Left](images/RetroMouse/Retro_Left.png)                | Left Button   |
| ![Retro_Middle](images/RetroMouse/Retro_Middle.png)             | Middle Button |
| ![Retro_Right](images/RetroMouse/Retro_Right.png)               | Right Button  |
|                                                                 | Start         |

## Compatibility

Please file bugs that are reproducible on upstream standalone on the [official forums](https://forum.fobby.net/index.php?t=msg&goto=4414&).

## External Links

* [Libretro Repository](https://github.com/libretro/beetle-saturn-libretro)
* [Report Core Issues Here](https://github.com/libretro/libretro-meta)
* [Official Website](https://mednafen.github.io/)
* [Official Upstream Downloads](https://mednafen.github.io/releases/)
