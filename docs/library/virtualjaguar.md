# Atari Jaguar (Virtual Jaguar)

## Background

Virtual Jaguar is a portable Jaguar emulator which is based on the source code of what used to be Potato Emulation.

Author(s): David Raingeard|Shamus

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/virtualjaguar.md). Changes are proposed using "Pull Requests."

## License

GPLv3

## Extensions

j64|jag|rom|abs|cof|bin|prg

## BIOS

The Virtual Jaguar core does not feature BIOS use.

## Features

| Saves | States      | Rewind | Netplay | RetroAchievements | RetroArch Cheats | Native Cheats |
|:-----:|:-----------:|:------:|:-------:|:-----------------:|:----------------:|:-------------:|
|  yes  |    no       |  no    |  no     |       no          |  no              | no            |

| Controllers     | Rumble | Sensors | Camera | Location | Subsystem     |
|:---------------:|:------:|:-------:|:------:|:--------:|:-------------:|
|       no        |   no   |   no    |  no    |    no    |      no       |

## Options

The Virtual Jaguar core has the following options that can be tweaked from the core options menu. The default setting is bolded.

- **Fast Blitter** (**Off**/On): this option will force Virtual Jaguar to use the older, less compatible yet faster blitter. Some games will not work properly with this option checked.
- **Doom Res Hack** (**Off**/On): Needed for Doom to run in its correct resolution.

??? note "*Doom Res Hack - Disabled*"
    ![doom_res_hack_disabled](images\Cores\virtualjaguar\doom_res_hack_disabled.png)

??? note "*Doom Res Hack - Enabled*"
    ![doom_res_hack_disabled](images\Cores\virtualjaguar\doom_res_hack_enabled.png)

- **Bios (Restart)** (**Off**/On): Enables bios loading sequence.

??? note "*Bios - Enabled*"
    ![Bios_enabled](images\Cores\virtualjaguar\Bios_enabled.png)

- **Pal (Restart)** (**Off**/On): NTSC to PAL switch. Setting this to on switches to PAL mode.

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

A reference compatibility table can be found on the bottom of this [page](https://icculus.org/virtualjaguar/)

| Game               | Issue                                                 |
|--------------------|-------------------------------------------------------|
|**Cybermorph**      |Graphics glitches. (1)                                 |
|**Doom**            |Enable Doom core option hack for proper graphics pitch.|
|**Iron Soldier**    |Hangs after selecting a stage.                         |
|**Iron Soldier 2**  |Hangs after selecting a stage. Audio glitches.         |
|**Kasumi Ninja**    |Graphics glitches. Missing background layers (2)       |
|**Ruiner Pinball**  |Doesn't boot.                                          |
|**Super Burnout**   |Hangs after selecting a track.                         |
|**Towers II**       |Heavy flickering.                                      |
|**Wolfenstein 3D**  |Doesn't boot.                                          |

??? note "*(1)*"
    ![Fault](images\Compatibility\virtualjaguar-Cybermorph.png)

??? note "*(2)*"
    ![Fault](images\Compatibility\virtualjaguar-Kasumi_Ninja)

## External Links

* [Libretro Repository](https://github.com/libretro/virtualjaguar-libretro)
* [Report Core Issues Here](https://github.com/libretro/libretro-meta/issues)
* [Official Website](https://icculus.org/virtualjaguar/)
* [Upstream Git Repository](http://shamusworld.gotdns.org/git/virtualjaguar)
