# Game Boy / Game Boy Color (TBG Dual)

## Background

TGB Dual is an open source (GPLv2) GB/GBC emulator with game link cable support. Authors: GIGO|Hii

## License

GPLv2

## Extensions

gb|gbc|sgb

## BIOS

TGB Dual does not support using BIOS image files.

## Feature Support
These are libretro features, not frontend or standalone emulator features.

##### Features:
| Saves | Save States | Rewind | Netplay | RetroAchievements | Cheats | Controllers |
|-------|-------------|--------|---------|-------------------|--------|-------------|
|   yes   |   yes  |    Yes   |    Yes   |    -    |         yes         |    no  |

| Rumble | Sensors | Camera | Location | Subsystem |
|--------|---------|--------|----------|-----------|
|    no   |    no    |    no   |     no    |     no     |

## Options

This core has a few options that can be tweaked from the core options menu. The default setting is bolded:

- **GB Link Enable** (**disabled**/enabled) (restart): Emulates two Game Boy units side by side for multiplayer support.
- **Screen placement** (**horizontal**/vertical): Switches the screen layout for multiplayer support.
- **Switch player screens** (**normal**/switched): Switches the player screens for multiplayer support.
- **Show player screens** (**both players**/player 1 only/player 2 only): Displays the selected player screens for multiplayer support.

## Controllers

![Game Boy Diagram](images/Controllers/Game-Boy_joypad.png)

The core supports controller setting:

* TGB Dual Joypad: Game Boy Controller

| [RetroPad](RetroPad)                                           | Joypad |
|----------------------------------------------------------------|--------|
| ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               |A button (right)|
| ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               |B button (down)|
| ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)               |dpad        |
| ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   |Prev Audio Mode        |
| ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              |        |
| ![RetroPad_L3](images/RetroPad/Retro_L3.png)                   |        |
| ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)   |        |
| ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   |Next Audio Mode        |
| ![RetroPad_R2](images/RetroPad/Retro_R2.png)                   |        |
| ![RetroPad_R3](images/RetroPad/Retro_R3.png)                   |        |
| ![RetroPad_Right_Stick](images/RetroPad/Retro_Right_Stick.png) |        |
| ![RetroPad_Select](images/RetroPad/Retro_Select.png)           |Select        |
| ![RetroPad_Start](images/RetroPad/Retro_Start.png)             |Start        |
| ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               |        |
| ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               |        |

## Compatibility

untested

## External Links

* [Official Website](http://gigo.retrogames.com/download.html)  
* [Libretro Repository](https://github.com/libretro/tgbdual-libretro)
* [Report Issues Here](https://github.com/libretro/libretro-meta)
