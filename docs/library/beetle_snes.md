# SNES / Super Famicom (Beetle bsnes)

**[This core currently doesn't start](https://github.com/libretro/beetle-bsnes-libretro/issues/3) so this documentation will remain incomplete until it is fixed.**

## Background

Standalone port of Mednafen bSNES to libretro, itself a old fork of bsnes 0.59.

### Why use this core?

This core exists as a side effect of porting/forking mednafen for its other cores in the past. There's no reason to use this core now that there's other more compatible and faster SNES cores.

### Author(s):

byuu|Mednafen Team

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/beetle_snes.md). Changes are proposed using "Pull Requests."

## See also

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

[Snes9x](https://buildbot.libretro.com/docs/library/snes9x)

## License

GPLv2

## Extensions

*Content that can be loaded by the Beetle bsnes core have the following file extensions.*

smc|fig|bs|st|sfc

## Database(s)

*RetroArch databases that are associated with the Beetle bsnes core*

* Nintendo - Super Nintendo Entertainment System

* Nintendo - Super Nintendo Entertainment System Hacks

* Nintendo - Sufami Turbo

## BIOS

The Beetle bsnes core does not feature BIOS use.

## Features

| Feature           | Supported |
|-------------------|:---------:|
| Saves             | -         |
| States            | -         |
| Rewind            | -         |
| Netplay           | -         |
| RetroAchievements | -         |
| RetroArch Cheats  | -         |
| Native Cheats     | ✕         |
| Controllers       | -         |
| Multi-Mouse       | -         |
| Rumble            | ✕         |
| Sensors           | ✕         |
| Camera            | ✕         |
| Location          | ✕         |
| Subsystem         | ✕         |

The Beetle bsnes core creates directories named 'Mednafen bSNES' in RetroArch's...

* Savefile directory when the core is loaded.
* Statestate directory when the core is loaded.
* Config directory when a Core Override or a Game Override or a Game-options file is saved.
* Input Remapping directory when a Core Remap or a Game Remap is saved.
* Shaders Presets directory when a Core Preset or a Game Preset is saved.

Core Overrides/Remaps/Presets that are saved will be named 'Mednafen bSNES'. 

Game Overrides/Remaps/Presets and Game-option files will have the same name as the loaded content.

## Options

The Beetle bsnes core does not feature core options.

## Controllers

*The Beetle bsnes core supports the following controller setting(s), bolded controller settings are the default for the specified user(s):*

### User # Device Type(s)

* **RetroPad** - Joypad without analog

| Beetle bsnes | RetroPad                                                       |
|--------------|----------------------------------------------------------------|
| B            | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               |
| Y            | ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               |
| Select       | ![RetroPad_Select](images/RetroPad/Retro_Select.png)           |
| Start        | ![RetroPad_Start](images/RetroPad/Retro_Start.png)             |
| Up           | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Up.png)            |
| Down         | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Down.png)          |
| Left         | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Left.png)          |
| Right        | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Right.png)         |
| A            | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               |
| X            | ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               |
| L            | ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   |
| R            | ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   |

## Compatibility

Unknown

## External Links

* [Libretro Repository](https://github.com/libretro/beetle-bsnes-libretro)
* [Report Core Issues Here](https://github.com/libretro/libretro-meta)
* [Official Website](https://mednafen.github.io/)
* [Official Upstream Downloads](https://mednafen.github.io/releases/)
