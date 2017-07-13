# Game Boy/Game Boy Color (Emux)

## Background
Emux is a cross-platform emulator project with a goal of emulating multiple kinds of machines related to gaming, such as consoles or arcades. Its philosophy is very much inspired by the Linux kernel (hence the name), which brilliantly manages to support multiple machines while keeping drivers entirely platform-independent. Emux is designed in the same way, keeping a code base of CPUs and controllers separate from machines. |Author:- Sebastien Ronsse

## License
GPLv2
## Extensions
gb|bin|rom
## BIOS
Emux does not support using BIOS image files.
## Feature Support
These are libretro features, not frontend or standalone emulator features.

##### Features:
| Saves | Save | states | Rewind | Netplay | RetroAchievements | Cheats | Controllers |
|-------|------|--------|--------|---------|-------------------|--------|-------------|
| yes   |   -  |    -   |    -   |    -    |         -         |    -   |      -      |

| Rumble | Sensors | Camera | Location | Subsystem |
|--------|---------|--------|----------|-----------|
|    -   |    -    |    -   |     -    |     -     |

## Options

This core does not feature core options.

## Controllers

![Game Boy Diagram](images/Controllers/Game-Boy_joypad.png)

The core supports controller setting:
* Joypad: Game Boy Controller

| [RetroPad](RetroPad)                                           | Joypad |
|----------------------------------------------------------------|--------|
| ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               |        |
| ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               |        |
| ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)               | dpad   |
| ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   |        |
| ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              |        |
| ![RetroPad_L3](images/RetroPad/Retro_L3.png)                   |        |
| ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)   |        |
| ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   |        |
| ![RetroPad_R2](images/RetroPad/Retro_R2.png)                   |        |
| ![RetroPad_R3](images/RetroPad/Retro_R3.png)                   |        |
| ![RetroPad_Right_Stick](images/RetroPad/Retro_Right_Stick.png) |        |
| ![RetroPad_Select](images/RetroPad/Retro_Select.png)           |        |
| ![RetroPad_Start](images/RetroPad/Retro_Start.png)             |        |
| ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               |        |
| ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               |        |

## Compatibility

untested

## External Links

* [Official Repository](https://github.com/sronsse/emux)  
* [Libretro Repository](https://github.com/libretro/emux)
* [Report Issues Here](http://github.com/libretro/libretro-meta/issues)
