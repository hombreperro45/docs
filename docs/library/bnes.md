# NES / Famicom (bnes)

## Background

A port of bNES v083 to libretro.

Author(s):

byuu|Ryphecha

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/bnes.md). Changes are proposed using "Pull Requests."

## License

GPLv3

## Extensions

nes

## BIOS

The bnes core does not feature BIOS use.

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
| Multi-Mouse       | ✕         |
| Rumble            | ✕         |
| Sensors           | ✕         |
| Camera            | ✕         |
| Location          | ✕         |
| Subsystem         | ✕         |

The bnes core creates directories named 'bnes' in RetroArch's save and state directories

Game data is saved/loaded to and from the core's save directory 

Save states are saved/loaded to and from the core's state directory.

## Options

The bnes core does not feature core options.

## Controllers

The bnes core supports 2 controller setting(s), the bolded controller setting is default:

The bnes core supports a max of 4 users.

### Device Types available to all users

* **RetroPad** - [Joypad without analog] - Nintendo Entertainment System Controller.

* RetroPad w/Analog - [Joypad with Analog] - No reason to use this.

| bnes          | **RetroPad**                                               |
|---------------|------------------------------------------------------------|
| B             | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)           |
| Select button | ![RetroPad_Select](images/RetroPad/Retro_Select.png)       |
| Start button  | ![RetroPad_Start](images/RetroPad/Retro_Start.png)         |
| D-Pad Up      | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Up.png)        |
| D-Pad Down    | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Down.png)      |
| D-Pad Left    | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Left.png)      |
| D-Pad Right   | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Right.png)     |
| A             | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)           |

## Compatibility

| Game                         | Issue                                          |
|------------------------------|------------------------------------------------|
| Crisis Force                 | Graphical glitches. (1)                        |
| Huge Insect                  | No enemies spawn.                              |
| Lagrange Point               | No music.                                      |
| Ms. Pac-Man (Tengen version) | Graphical glitches on the sides of the screen. |
| Skull & Crossbones           | Crashes on start.                              |

??? note "(1)"
    ![crisiscore_graphicalglitches](images/cores/bnes/crisiscore_graphicalglitches.png)

## External Links

* [Libretro Repository](https://github.com/libretro/bnes-libretro)
* [Report Core Issues Here](https://github.com/libretro/libretro-meta)
* [Official Website](https://byuu.org/)
* [Official Upstream Downloads](https://byuu.org/emulation/higan/)
