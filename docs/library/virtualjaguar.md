# Atari Jaguar (Virtual Jaguar)

## Background

Virtual Jaguar is a portable Jaguar emulator which is based on the source code of what used to be Potato Emulation.

Author(s): David Raingeard|Shamus

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/virtualjaguar.md). Changes are proposed using "Pull Requests."

## License

GPLv3

## Extensions

j64|jag

## BIOS

The Virtual Jaguar core does not feature BIOS use.

## Feature Support

These are libretro features, not frontend or standalone emulator features.

| Saves | States      | Rewind | Netplay | RetroAchievements | Cheats |
|:-----:|:-----------:|:------:|:-------:|:-----------------:|:------:|
|  yes  |    no       |  no    |  no     |       no          |  no    |

| Controllers     | Rumble | Sensors | Camera | Location | Subsystem     |
|:---------------:|:------:|:-------:|:------:|:--------:|:-------------:|
|       no        |   no   |   no    |  no    |    no    |      no       |

## Options

The Virtual Jaguar core has the following options that can be tweaked from the core options menu. The default setting is bolded.

- **Fast Blitter** (**Off**/On): Use a faster, but less accurate blitter.
- **Doom Res Hack** (**Off**/On): Needed for Doom to run in its correct resolution..
- **Bios** (**Off**/On): Enables bios loading sequence.
- **Pal (Restart)** (**Off**/On): Awaiting Description.

## Controllers

The Virtual Jaguar core supports one controller setting(s):

* RetroPad

![virtualjaguar_retropad](images\Controllers\virtualjaguar_retropad.png)

| Virtual Jaguar | [RetroPad](RetroPad)                                           |
|----------------|----------------------------------------------------------------|
| B              | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               |
| C              | ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               |
| Pause          | ![RetroPad_Select](images/RetroPad/Retro_Select.png)           |
| Option         | ![RetroPad_Start](images/RetroPad/Retro_Start.png)             |
| D-Pad          | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)               |    
| A              | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               |
| Numpad 0       | ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               |
| Numpad 1       | ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   |
| Numpad 2       | ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   |
| Numpad 3       | ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              |
| Numpad 4       | ![RetroPad_R2](images/RetroPad/Retro_R2.png)                   |
| Numpad 5       | ![RetroPad_L3](images/RetroPad/Retro_L3.png)                   |
| Numpad 6       | ![RetroPad_R3](images/RetroPad/Retro_R3.png)                   |
|                | ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)   |
|                | ![RetroPad_Right_Stick](images/RetroPad/Retro_Right_Stick.png) |

## Compatibility

A compatibility table can be found on the bottom of this [page](https://icculus.org/virtualjaguar/)

## External Links

* [Libretro Repository](https://github.com/libretro/virtualjaguar-libretro)
* [Report Libretro Issues Here](https://github.com/libretro/libretro-meta/issues)
* [Official Website](https://icculus.org/virtualjaguar/)
* [Upstream Git Repository](http://shamusworld.gotdns.org/git/virtualjaguar)
