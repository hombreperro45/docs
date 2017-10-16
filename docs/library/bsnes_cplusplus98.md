# SNES / Super Famicom (bsnes C++98 (v085))

## Background

bsnes c++98 is a special fork from around v085 that's been backported to work with older compilers. Many platforms LibRetro supports such as various consoles (PlayStation 3) are stuck with super-old compilers that don't support the latest c++ features that are in the newer bsnes v094 ports.

Author(s):

byuu|Themaister|Ver GreenEyes

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/bsnes_cplusplus98.md). Changes are proposed using "Pull Requests."

## See also

[bsnes_accuracy](https://buildbot.libretro.com/docs/library/bsnes_accuracy/)

[bsnes_balanced](https://buildbot.libretro.com/docs/library/bsnes_balanced/)

[bsnes_performance](https://buildbot.libretro.com/docs/library/bsnes_performance/)

## License

GPLv3

## Extensions

sfc|smc

## BIOS

The bsnes C++98 (v085) core does not feature BIOS use.

## Features

| Feature           | Supported |
|-------------------|:---------:|
| Saves             | ✔         |
| States            | ✔         |
| Rewind            | ✔         |
| Netplay           | ✔         |
| RetroAchievements | ✕         |
| RetroArch Cheats  | -         |
| Native Cheats     | ✕         |
| Controllers       | ✕         |
| Multi-Mouse       | ✕         |
| Rumble            | ✕         |
| Sensors           | ✕         |
| Camera            | ✕         |
| Location          | ✕         |
| Subsystem         | -         |

The bsnes C++98 (v085) core creates directories named 'bsnes' in RetroArch's save and state directories

Game data is saved/loaded to and from the core's save directory.

Save states are saved/loaded to and from the core's state directory. 

## Options

The bsnes C++98 (v085) core does not feature core options.

## Controllers

The bsnes C++98 (v085) supports 6 controller setting(s), the bolded controller setting is default:

The bsnes C++98 (v085) core supports a max of 5 users.

### User 1 and 2 exclusive Device Types

* **[SNES Joypad](http://nintendo.wikia.com/wiki/Super_Nintendo_Entertainment_System_controller)** - [Joypad without analog]

* [SNES Mouse](https://en.wikipedia.org/wiki/Super_NES_Mouse) - [Mouse]

### User 2 exclusive Device Types

* [Multitap](http://nintendo.wikia.com/wiki/Super_Multitap) - [Joypad] - allows for up to five players to play together in certain games.

* [SuperScope](https://en.wikipedia.org/wiki/Super_Scope) - [Lightgun]

* [Justifier](https://en.wikipedia.org/wiki/Konami_Justifier) - [Lightgun]

* [Justifiers](https://en.wikipedia.org/wiki/Konami_Justifier) - [Lightgun]

| bsnes C++98 (v085) | RetroPad                                               | SNES Joypad                                             |
|----------------|--------------------------------------------------------|---------------------------------------------------------|
| B              | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)       | ![SNES_B](images/Button_Pack/SNES/SNES_B.png)           |
| Y              | ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)       | ![SNES_Y](images/Button_Pack/SNES/SNES_Y.png)           |
| Select         | ![RetroPad_Select](images/RetroPad/Retro_Select.png)   | ![SNES_Select](images/Button_Pack/SNES/SNES_Select.png) |
| Start          | ![RetroPad_Start](images/RetroPad/Retro_Start.png)     | ![SNES_Start](images/Button_Pack/SNES/SNES_Start.png)   |
| D-Pad Up       | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Up.png)    | ![SNES_Dpad](images/Button_Pack/SNES/SNES_Dpad.png)     |
| D-Pad Down     | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Down.png)  | ![SNES_Dpad](images/Button_Pack/SNES/SNES_Dpad.png)     |
| D-Pad Left     | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Left.png)  | ![SNES_Dpad](images/Button_Pack/SNES/SNES_Dpad.png)     |
| D-Pad Right    | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Right.png) | ![SNES_Dpad](images/Button_Pack/SNES/SNES_Dpad.png)     |
| A              | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)       | ![SNES_A](images/Button_Pack/SNES/SNES_A.png)           |
| X              | ![RetroPad_X](images/RetroPad/Retro_X_Round.png)       | ![SNES_X](images/Button_Pack/SNES/SNES_X.png)           |
| L              | ![RetroPad_L1](images/RetroPad/Retro_L1.png)           | ![SNES_L](images/Button_Pack/SNES/SNES_L.png)           |
| R              | ![RetroPad_R1](images/RetroPad/Retro_R1.png)           | ![SNES_R](images/Button_Pack/SNES/SNES_R.png)           |

| RetroMouse                                                                                                      | SNES Mouse   | SuperScope | Justifier(s) |
|-----------------------------------------------------------------------------------------------------------------|--------------|------------|--------------|
| ![Retro_Mouse](images/RetroMouse/Retro_Mouse.png)                                                               | Pointer      | Pointer    | Pointer      |
| ![Retro_Left](images/RetroMouse/Retro_Left.png)                                                                 | Left Button  | Trigger    | Trigger      |
| ![Retro_Middle](images/RetroMouse/Retro_Middle.png)                                                             |              | ???        |              |
| ![Retro_Right](images/RetroMouse/Retro_Right.png)                                                               | Right Button | Turbo      | Turbo        |
| ![Retro_Left+Middle](images/RetroMouse/Retro_Left+Middle.png)                                                   |              | Pause      | Pause        |
| ![Retro_Right+Middle](images/RetroMouse/Retro_Right+Middle.png)                                                 |              | Start      | Start        |
| ![Retro_Left+Middle](images/RetroMouse/Retro_Left+Middle.png) + ![Retro_Left](images/RetroMouse/Retro_Left.png) |              | Reset      | Reset        |

## Compatibility

Unknown

## External Links

* [Libretro Repository](https://github.com/libretro/bsnes-libretro-cplusplus98)
* [Report Core Issues Here](https://github.com/libretro/libretro-meta)
* [Official Website](https://byuu.org/)
* [Official Upstream Downloads](https://byuu.org/emulation/higan/)