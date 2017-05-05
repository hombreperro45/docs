# Sega Saturn (Yabause)

![Yabause_Banner](images/Banners/Yabause_Banner.png)

## Background

Yabause (Yet Another Buggy And Uncomplete Saturn Emulator) is the only active Sega Saturn emulator that is both open-source and written with portability in mind. The libretro port only supports the software renderer at the moment, which is more accurate but also slower than the GL renderer.
## License

GPLv2

## Extensions

iso|cue|bin

## BIOS

|   Filename    |    Description     |              md5sum              |
|:-------------:|:------------------:|:--------------------------------:|
|saturn_bios.bin|  Sega Saturn BIOS  | af5828fdff51384f99b3c4926be27762 |

## Feature Support

These are libretro features, not frontend or standalone emulator features.

| Saves | Save states | Rewind | Netplay | RetroAchievements | Cheats  |
|:-----:|:-----------:|:------:|:-------:|:-----------------:|:-------:|
|  yes  |      no     |   no   |   no    |         no        |   yes   |

| Controllers API | Rumble | Sensors | Camera | Location | Subsystem API |
|:---------------:|:------:|:-------:|:------:|:--------:|:-------------:|
|       yes       |   no   |    no   |   no   |    no    |       no      |

## Options

|   Core Option   |         Description                                                        | Options (Default Bolded) | Requires Restart |
|:---------------:|:--------------------------------------------------------------------------:|:------------------------:|:----------------:|
|    Frameskip    | Frames are skipped when the CPU is unable to keep up a stable rate         |        **Off**/On        |        No        |
| Force HLE BIOS  | HLE BIOS will be used even when a real BIOS file is present                |         Off/**On**       | Yes              |
| Addon Cartridge | Allows switching between the various RAM cartridges released for the system| **none**/1M_ram/4M_ram   | Yes              |

## Controllers

The core supports controller setting:

* Joypad: Controller

![Saturn_joypad_diagram](images\Controllers\Yabause_joypad.png)

|                      [RetroPad](RetroPad)                      |   Saturn Joypad   |
|:--------------------------------------------------------------:|:--------------:|
|        ![RetroPad_A](images/RetroPad/Retro_A_Round.png)        |        B       |
|        ![RetroPad_B](images/RetroPad/Retro_B_Round.png)        |        A       |
|        ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)        |      D-pad     |
|          ![RetroPad_L1](images/RetroPad/Retro_L1.png)          |        C       |
|          ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)     | Left Shoulder  |
|          ![RetroPad_L3](images/RetroPad/Retro_L3.png)          |                |
|  ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)  |   Analog X/Y   |
|          ![RetroPad_R1](images/RetroPad/Retro_R1.png)          |        Z       |
|          ![RetroPad_R2](images/RetroPad/Retro_R2.png)          | Right Shoulder |
|          ![RetroPad_R3](images/RetroPad/Retro_R3.png)          |                |
| ![RetroPad_Right_Stick](images/RetroPad/Retro_Right_Stick.png) |                |
|      ![RetroPad_Select](images/RetroPad/Retro_Select.png)      |                |
|       ![RetroPad_Start](images/RetroPad/Retro_Start.png)       |      Start     |
|        ![RetroPad_X](images/RetroPad/Retro_X_Round.png)        |        Y       |
|        ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)        |        A       |

## External Links

* [Official Website](https://yabause.org/)
* [Official GitHub Repository](https://github.com/Guillaumito/yabause)
* [Libretro Repository](https://github.com/libretro/4do-libretro)
