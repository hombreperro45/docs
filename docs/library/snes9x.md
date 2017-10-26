# SNES / Super Famicom (Snes9x)

## Background

Port of upstream up-to-date mainline Snes9x, a portable Super Nintendo Entertainment System emulator to libretro.

### Why use this core?

* Highly accurate SNES emulation.

* Simplified and easily accessible MSU-1 expansion chip support.

* Recommended for netplay

* Less CPU intensive but less compatible than the higan based cores.

### Author(s):

Snes9x Team

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/snes9x.md). Changes are proposed using "Pull Requests."

## See also

[Beetle bsnes](https://buildbot.libretro.com/docs/library/beetle_bsnes)

[bsnes Accuracy](https://buildbot.libretro.com/docs/library/bsnes_accuracy)

[bsnes Balanced](https://buildbot.libretro.com/docs/library/bsnes_balanced)

[bsnes C++98 (v085)](https://buildbot.libretro.com/docs/library/bsnes_cplusplus98)

[bsnes Performance](https://buildbot.libretro.com/docs/library/bsnes_performance)

[bsnes-mercury Accuracy](https://buildbot.libretro.com/docs/library/bsnes_mercury_accuracy)

[bsnes-mercury Balanced](https://buildbot.libretro.com/docs/library/bsnes_mercury_balanced)

[bsnes-mercury Performance](https://buildbot.libretro.com/docs/library/bsnes_mercury_performance)

[higan Accuracy](https://buildbot.libretro.com/docs/library/higan_accuracy)

[Snes9x 2002](https://buildbot.libretro.com/docs/library/snes9x_2002)

[Snes9x 2005 Plus](https://buildbot.libretro.com/docs/library/snes9x_2005_plus)

[Snes9x 2005](https://buildbot.libretro.com/docs/library/snes9x_2005)

[Snes9x 2010](https://buildbot.libretro.com/docs/library/snes9x_2010)

## License

Non-commercial

## Extensions

*Content that can be loaded by the Snes9x core have the following file extensions.*

smc|sfc|swc|fig

## Database(s)

*RetroArch databases that are associated with the Snes9x core*

* Nintendo - Super Nintendo Entertainment System

* Nintendo - Super Nintendo Entertainment System Hacks

* Nintendo - Sufami Turbo

## BIOS

The Snes9x core does not feature BIOS use.

## Features

| Feature           | Supported |
|-------------------|:---------:|
| Saves             | ✓         |
| States            | ✓         |
| Rewind            | ✓         |
| Netplay           | ✓         |
| RetroAchievements | ✓         |
| RetroArch Cheats  | ✓         |
| Native Cheats     | ✕         |
| Controllers       | ✓         |
| Multi-Mouse       | -         |
| Rumble            | ✕         |
| Sensors           | ✕         |
| Camera            | ✕         |
| Location          | ✕         |
| Subsystem         | ✕         |

The Snes9x core creates directories named 'Snes9x' in RetroArch's...

* Savefile directory when the core is loaded.
* Statestate directory when the core is loaded.
* Config directory when a Core Override or a Game Override or a Game-options file is saved.
* Input Remapping directory when a Core Remap or a Game Remap is saved.
* Shaders Presets directory when a Core Preset or a Game Preset is saved.

Core Overrides/Remaps/Presets that are saved will be named 'Snes9x'.

Game Overrides/Remaps/Presets and Game-option files will have the same name as the loaded content.

Game data is saved/loaded to and from the core's save directory.

Save states are saved/loaded to and from the core's state directory.

## Options

*The Snes9x core has the following options that can be tweaked from the core options menu. The default setting is bolded.*

- **SuperFX Frequency** (**10MHz**/20MHz/40MHz/60MHz/80MHz/100MHz): Overclock the [SuperFX chip](https://en.wikipedia.org/wiki/Super_FX).
- **Show layer 1** (**On**/Off): Self-explanatory.
- **Show layer 2** (**On**/Off): Self-explanatory.
- **Show layer 3** (**On**/Off): Self-explanatory.
- **Show layer 4** (**On**/Off): Self-explanatory.
- **Show sprite layer** (**On**/Off): Self-explanatory.
- **Enable graphic clip windows** (**On**/Off): Self-explanatory.
- **Enable transparency effects** (**On**/Off): Self-explanatory.
- **Enable sound channel 1** (**On**/Off): Self-explanatory.
- **Enable sound channel 2** (**On**/Off): Self-explanatory.
- **Enable sound channel 3** (**On**/Off): Self-explanatory.
- **Enable sound channel 4** (**On**/Off): Self-explanatory.
- **Enable sound channel 5** (**On**/Off): Self-explanatory.
- **Enable sound channel 6** (**On**/Off): Self-explanatory.
- **Enable sound channel 7** (**On**/Off): Self-explanatory.
- **Enable sound channel 8** (**On**/Off): Self-explanatory.
- **Crop overscan** (**auto**/On/Off): Self-explanatory.
- **Preferred aspect ratio** (**auto**/ntsc/pal/4:3): Choose the preferred aspect ratio. RetroArch's aspect ratio must be set to Core provided in the Video seetings.

## Controllers

*The Snes9x core supports the following controller setting(s), bolded controller settings are the default for the specified user(s):*

### User 1 Device Type(s)

* **[SNES Joypad](http://nintendo.wikia.com/wiki/Super_Nintendo_Entertainment_System_controller)** - Joypad without analog

* [SNES Mouse](https://en.wikipedia.org/wiki/Super_NES_Mouse) - Mouse

* [Multitap](http://nintendo.wikia.com/wiki/Super_Multitap) - Joypad without analog - allows for up to five players to play together in certain games.

### User 2 Device Type(s)

* **[SNES Joypad](http://nintendo.wikia.com/wiki/Super_Nintendo_Entertainment_System_controller)** - Joypad without analog

* [SNES Mouse](https://en.wikipedia.org/wiki/Super_NES_Mouse) - Mouse

* [Multitap](http://nintendo.wikia.com/wiki/Super_Multitap) - Joypad without analog - allows for up to five players to play together in certain games.

* [SuperScope](https://en.wikipedia.org/wiki/Super_Scope) - Lightgun

* [Justifier](https://en.wikipedia.org/wiki/Konami_Justifier) - Lightgun

### User 3 - 16 Device Type(s)

* **RetroPad** - Joypad without analog

### Controllers graph

| Snes9x      | RetroPad                                                       | *SNES Joypad / Multitap*                                |
|-------------|----------------------------------------------------------------|---------------------------------------------------------|
| B           | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               | ![SNES_B](images/Button_Pack/SNES/SNES_B.png)           |
| Y           | ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               | ![SNES_Y](images/Button_Pack/SNES/SNES_Y.png)           |
| Select      | ![RetroPad_Select](images/RetroPad/Retro_Select.png)           | ![SNES_Select](images/Button_Pack/SNES/SNES_Select.png) |
| Start       | ![RetroPad_Start](images/RetroPad/Retro_Start.png)             | ![SNES_Start](images/Button_Pack/SNES/SNES_Start.png)   |
| D-Pad Up    | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Up.png)            | ![SNES_Dpad](images/Button_Pack/SNES/SNES_Dpad.png)     |
| D-Pad Down  | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Down.png)          | ![SNES_Dpad](images/Button_Pack/SNES/SNES_Dpad.png)     |
| D-Pad Left  | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Left.png)          | ![SNES_Dpad](images/Button_Pack/SNES/SNES_Dpad.png)     |
| D-Pad Right | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Right.png)         | ![SNES_Dpad](images/Button_Pack/SNES/SNES_Dpad.png)     |
| A           | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               | ![SNES_A](images/Button_Pack/SNES/SNES_A.png)           |
| X           | ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               | ![SNES_X](images/Button_Pack/SNES/SNES_X.png)           |
| L           | ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   | ![SNES_L](images/Button_Pack/SNES/SNES_L.png)           |
| R           | ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   | ![SNES_R](images/Button_Pack/SNES/SNES_R.png)           |

| RetroMouse                                                      | *SNES Mouse* | *SuperScope* | *Justifier* |
|-----------------------------------------------------------------|--------------|--------------|-------------|
| ![Retro_Mouse](images/RetroMouse/Retro_Mouse.png)               | Pointer      | Pointer      | Pointer     |
| ![Retro_Left](images/RetroMouse/Retro_Left.png)                 | Left Button  | ???          | ???         |
| ![Retro_Middle](images/RetroMouse/Retro_Middle.png)             |              | ???          | ???         |
| ![Retro_Right](images/RetroMouse/Retro_Right.png)               | Right Button | ???          | ???         |
| ![Retro_Left+Middle](images/RetroMouse/Retro_Left+Middle.png)   |              | ???          | ???         |
| ![Retro_Right+Middle](images/RetroMouse/Retro_Right+Middle.png) |              | ???          | ???         |


## Compatibility

| Game                                             | Issue                                                                                |
|--------------------------------------------------|--------------------------------------------------------------------------------------|
| A.S.P. Air Strike Patrol                         | The shadow below the aircraft is missing. Glitched graphics on the briefing screens. |
| BS-Zelda MottZilla Patch                         | Only shows a black screen.                                                           |
| Doom                                             | Colored dots appear during gameplay.                                                 |
| Funaki Masakatsu Hybrid Wrestler – Tougi Denshou | Corrupted graphics on the Pancrase logo screen.                                      |
| Hayazashi Nidan Morita Shougi 2                  | Matches won’t start.                                                                 |
| Mecarobot Golf                                   | The ground "wobbles" during gameplay.                                                |
| Secret of Evermore (PAL versions)                | Randomly freezes when the background music changes.                                  |
| Speedy Gonzales: Los Gatos Bandidos              | Freezes when pressing a switch in the last level.                                    |

* Snes9x can launch some Satellaview games with sometimes low compatibility.

### MSU-1 Support

-

## External Links

* [Libretro Repository](https://github.com/libretro/snes9x)
* [Report Core Issues Here](https://github.com/libretro/libretro-meta/labels/core:%20snes9x)
* [Official Website (no longer updated)](http://www.snes9x.com/)
* [Official Repository](https://github.com/snes9xgit/snes9x)
* [Official Upstream Downloads](http://www.s9x-w32.de/dl/)
