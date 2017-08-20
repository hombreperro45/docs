# Sega MS/GG/MD/CD (Genesis Plus GX)

## Background

Genesis Plus GX is an open-source Sega 8/16 bit emulator focused on accuracy and portability. The source code, originally based on Genesis Plus 1.3 by Charles MacDonald, has been heavily modified & enhanced, with respect to initial goals and design, in order to improve the accuracy of emulation, implementing new features and adding support for extra peripherals, cartridge & systems hardware.

Author(s): Charles McDonald|Eke-Eke

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/blob/master/docs/library/genesis_plus_gx.md). Changes are proposed using "Pull Requests."

## License

Non-commercial

## Extensions

mdx|md|smd|gen|bin|cue|iso|sms|gg|sg

## BIOS

|   Filename    |    Description     |              md5sum              |
|:-------------:|:------------------:|:--------------------------------:|
| bios_CD_E.bin | MegaCD EU BIOS     |                                  |
| bios_CD_U.bin | SegaCD US BIOS     |                                  |
| bios_CD_J.bin | MegaCD JP BIOS     |                                  |
| bios_E.sms    | MasterSystem EU BIOS |                                |
| bios_U.sms    | MasterSystem US BIOS |                                |
| bios_J.sms    | MasterSystem JP BIOS |                                |
| bios.gg       | GameGear BIOS |                                       |
| sk.bin        | Sonic & Knuckles ROM | 4ea493ea4e9f6c9ebfccbdb15110367e |
| sk2chip.bin   | Sonic & Knuckles UPMEM ROM | b4e76e416b887f4e7413ba76fa735f16 |
| areplay.bin   | Action Replay ROM |                                   |
| ggenie.bin    | Game Genie ROM |                                      |

## Feature Support

These are libretro features, not frontend or standalone emulator features.

##### Features:

| Saves | States      | Rewind | Netplay | RetroAchievements | Cheats |
|:-----:|:-----------:|:------:|:-------:|:-----------------:|:------:|
|  yes  |   yes       | yes    |  yes    |       -           | yes    |

| Controllers     | Rumble | Sensors | Camera | Location | Subsystem     |
|:---------------:|:------:|:-------:|:------:|:--------:|:-------------:|
|      yes        |  no    |   no    |  no    |   no     |      no       |

## Options

|   Core Option   |         Description         | Options (Default Bolded) | Requires Restart |
|:---------------:|:---------------------------:|:------------------------:|:----------------:|
| System hardware | Choose which system is going to be emulated. | **auto**/sg-1000/sg-1000 II/mark-III/master system/master system II/game gear/mega drive / genesis | yes |
| System region | Choose which region the system is from. | **auto**/ntsc-u/pal/ntsc-j | yes |
| System lookups | Emulate system lockups | **enabled**/disabled | - |
| System bootrom | - | enabled/**disabled** | - |
| CD System BRAM | - | **per bios**/per game | - |
| 68k address error | Emulate the 68k address error. | **enabled**/disabled | - |
| Cartridge lock-on | Select lock-on cartridge. | **disabled**/game genie/action replay (pro)/sonic & knuckles | yes |
| Master System FM | Enable the Master System FM chip. | **auto**/disabled/enabled | - |
| YM2612 DAC quantization | Enable YM2612 DAC quantization | enabled/**disabled** | - |
| Blargg NTSC filter | Enable Blargg NTSC filters. | **disabled**/monochrome/composite/svidio/rgb | - |
| LCD Ghosting filter | - | enabled/**disabled** | - |
| Borders | Enable borders. | **disabled**/ top/bottom/ left/right / full | - |
| Game Gear extended screen | Extend the Game Gear screen. | enabled/**disabled** | - |
| Core-provided aspect ratio | - | **auto**/NTSC PAR/PAL PAR | - |
| Interlaced mode 2 output | Change how interlaced mode 2 output is handled | **single field**/double field | - |
| Show Lightgun crosshair | Self-explanatory | **no**/yes | - |
| Invert Mouse Y-axis | Self-explanatory | **no**/yes | - |

## Controllers

The Genesis Plus GX core supports sixteen different controller settings:

* Joypad Auto

* MD Joypad 3 Button

![3_button_genesis](images/Controllers/3_button_genesis_joypad.png)

* MD Joypad 6 Button

![6_button_genesis](images/Controllers/6_button_genesis_joypad.png)

* MS Joypad 2 Button (also used for Game Gear)

* MD Joypad 3 Button + 4-WayPlay

* MD Joypad 6 Button + 4-WayPlay

* MD Joypad 3 Button + Teamplayer

* MD Joypad 6 Button + Teamplayer

* MS Joypad 2 Button + Master Tap

* MS Light Phaser

* MS Paddle Control

* MS Graphic Board

* MS Sports Pad

* MD XE-1AP

* MD Mouse

* Joypad Port Empty

| [RetroPad](RetroPad)                                           | Joypad |
|----------------------------------------------------------------|--------|
| ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               |        |
| ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               |        |
| ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)               |        |
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

100% compatibility with Genesis / Mega Drive, Sega/Mega CD, Master System, Game Gear & SG-1000 released software (including all unlicensed or pirate known dumps), also emulating backwards compatibility modes when available.

## External Links

* [Libretro Repository](https://github.com/libretro/Genesis-Plus-GX)
* [Report Issues Here](http://github.com/libretro/libretro-meta/issues)
* [Official Website](https://github.com/ekeeke/Genesis-Plus-GX)
