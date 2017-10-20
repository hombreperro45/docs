# SNES / Super Famicom (Beetle bsnes)

## Background

Standalone port of Mednafen bSNES to libretro, itself a old fork of bsnes 0.59.

*[This core currently doesn't start](https://github.com/libretro/beetle-bsnes-libretro/issues/3) so this documentation will remain incomplete until it is fixed.*

### Author(s):

byuu|Mednafen Team

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/beetle_snes.md). Changes are proposed using "Pull Requests."

## See also

[bsnes Accuracy](https://buildbot.libretro.com/docs/library/bsnes_accuracy/)

[bsnes Balanced](https://buildbot.libretro.com/docs/library/bsnes_balanced/)

[bsnes Performance](https://buildbot.libretro.com/docs/library/bsnes_performance/)

[bsnes C++98 (v085)](https://buildbot.libretro.com/docs/library/bsnes_cplusplus98/)

## License

GPLv2

## Extensions

smc|fig|bs|st|sfc

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

The Beetle bsnes core creates directories named 'Mednafen bSNES' in RetroArch's save and state directories

## Options

The Beetle bsnes core does not feature core options.

## Controllers

The Beetle bsnes core supports - controller setting(s), the bolded controller setting is default:

The Beetle bsnes core supports a max of - users.

### Device Types available to all users

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
