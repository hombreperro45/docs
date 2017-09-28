# Game Boy/Game Boy Color (Emux)

## Background

Emux is a cross-platform emulator project with a goal of emulating multiple kinds of machines related to gaming, such as consoles or arcades. Its philosophy is very much inspired by the Linux kernel (hence the name), which brilliantly manages to support multiple machines while keeping drivers entirely platform-independent. Emux is designed in the same way, keeping a code base of CPUs and controllers separate from machines.

Author(s): Sebastien Ronsse

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/emux_gb.md). Changes are proposed using "Pull Requests."

## License

GPLv2

## Extensions

gb|bin|rom

## BIOS

|   Filename    |    Description                 |              md5sum              |
|:-------------:|:------------------------------:|:--------------------------------:|
| DMG_ROM.bin   | Game Boy Boot ROM - Required       | 32fbbd84168d3482956eb3c5051637f5 |

## Features

| Saves | States      | Rewind | Netplay | RetroAchievements | RetroArch Cheats | Native Cheats |
|:-----:|:-----------:|:------:|:-------:|:-----------------:|:----------------:|:-------------:|
|  yes  |     no      |   no   |  no     |        -          |   -              | no            |

| Controllers     | Rumble | Sensors | Camera | Location | Subsystem     |
|:---------------:|:------:|:-------:|:------:|:--------:|:-------------:|
|      yes        |  no    |   no    |  no    |   no     |      no       |

## Options

The Emux core does not feature core options.

## Controllers

The core supports one controller setting(s):

* RetroPad

![emux_gb_retropad](images/Controllers/emux_gb_retropad.png)

| Emux      | [RetroPad](RetroPad)                                           |
|-----------|----------------------------------------------------------------|
| B         | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               |
|           | ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               |
| Select    | ![RetroPad_Select](images/RetroPad/Retro_Select.png)           |
| Start     | ![RetroPad_Start](images/RetroPad/Retro_Start.png)             |
| D-pad     | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)               |
| A         | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               |
|           | ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               |
|           | ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   |
|           | ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   |
|           | ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              |
|           | ![RetroPad_R2](images/RetroPad/Retro_R2.png)                   |
|           | ![RetroPad_L3](images/RetroPad/Retro_L3.png)                   |
|           | ![RetroPad_R3](images/RetroPad/Retro_R3.png)                   |
|           | ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)   |
|           | ![RetroPad_Right_Stick](images/RetroPad/Retro_Right_Stick.png) |

## Compatibility

Unknown

## External Links

* [Libretro Repository](https://github.com/libretro/emux)
* [Report Core Issues Here](https://github.com/libretro/libretro-meta/issues)
* [Official Repository](https://github.com/sronsse/emux) 
