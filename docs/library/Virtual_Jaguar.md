# Atari Jaguar (Virtual Jaguar)

![Virtual-Jaguar_Banner](images/Banners/Virtual-Jaguar_banner.png)

## Background

Virtual Jaguar is a portable Jaguar emulator which is based on the source code of what used to be Potato Emulation.
## License

GPLv3

## Extensions

j64|jag

## BIOS

The libretro port of Virtual Jaguar does not support using BIOS image files.

## Feature Support

These are libretro features, not frontend or standalone emulator features.

| Saves | Save states | Rewind | Netplay | RetroAchievements | Cheats  |
|:-----:|:-----------:|:------:|:-------:|:-----------------:|:-------:|
|  yes  |      no     |   no   |   no    |         no        |   no    |

| Controllers API | Rumble | Sensors | Camera | Location | Subsystem API |
|:---------------:|:------:|:-------:|:------:|:--------:|:-------------:|
|       no       |   no   |    no   |   no   |    no    |       no      |

## Options

|   Core Option   |         Description                                                        | Options (Default Bolded) | Requires Restart |
|:---------------:|:--------------------------------------------------------------------------:|:------------------------:|:----------------:|
|   Fast Blitter  | Use a faster, but less accurate blitter         |        **Off**/On        |        No        |
| Doom Res Hack  |  Needed for Doom to run in its correct resolution.|         **Off**/On       | No              |
| Bios | Enables bios loading sequence| **Off**/On   | Yes              |
| PAL | Awaiting Description| **Off**/On   | Yes              |

## Controllers

The core supports controller setting:

* Joypad: Controller

![Atari_Jaguar_joypad_diagram](images\Controllers\Virtual-Jaguar_joypad.png)

|                      [RetroPad](RetroPad)                      |   Saturn Joypad   |
|:--------------------------------------------------------------:|:--------------:|
|        ![RetroPad_A](images/RetroPad/Retro_A_Round.png)        |        A       |
|        ![RetroPad_B](images/RetroPad/Retro_B_Round.png)        |        B       |
|        ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)        |      D-pad     |
|          ![RetroPad_L1](images/RetroPad/Retro_L1.png)          |    Numpad1     |
|          ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)     |    Numpad3     |
|          ![RetroPad_L3](images/RetroPad/Retro_L3.png)          |    Numpad5     |
|  ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)  |                |
|          ![RetroPad_R1](images/RetroPad/Retro_R1.png)          |    Numpad2     |
|          ![RetroPad_R2](images/RetroPad/Retro_R2.png)          |    Numpad4     |
|          ![RetroPad_R3](images/RetroPad/Retro_R3.png)          |    Numpad6     |
| ![RetroPad_Right_Stick](images/RetroPad/Retro_Right_Stick.png) |                |
|      ![RetroPad_Select](images/RetroPad/Retro_Select.png)      |     Pause      |
|       ![RetroPad_Start](images/RetroPad/Retro_Start.png)       |     Option     |
|        ![RetroPad_X](images/RetroPad/Retro_X_Round.png)        |    Numpad0     |
|        ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)        |        C       |

## External Links

* [Official Website](https://icculus.org/virtualjaguar/)
* [Official GitHub Repository](http://shamusworld.gotdns.org/git/virtualjaguar)
* [Libretro Repository](https://github.com/libretro/virtualjaguar-libretro)
* [Unofficial GitHub Mirror](https://github.com/mirror/virtualjaguar)
