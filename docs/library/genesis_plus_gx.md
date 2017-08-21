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
| bios_CD_E.bin | MegaCD EU BIOS - Required for EU | - |
| bios_CD_U.bin | SegaCD US BIOS - Required for US | - |
| bios_CD_J.bin | MegaCD JP BIOS - Required for JP | - |
| bios_E.sms    | MasterSystem EU BIOS - Optional | - |
| bios_U.sms    | MasterSystem US BIOS - Optional | - |
| bios_J.sms    | MasterSystem JP BIOS - Optional | - |
| bios.gg       | GameGear BIOS | - |
| sk.bin        | Sonic & Knuckles ROM - Optional | 4ea493ea4e9f6c9ebfccbdb15110367e |
| sk2chip.bin   | Sonic & Knuckles UPMEM ROM - Optional  | b4e76e416b887f4e7413ba76fa735f16 |
| areplay.bin   | Action Replay ROM - Optional | - |
| ggenie.bin    | Game Genie ROM - Optional | - |

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

- **System hardware (restart)** (**auto**/sg-1000/sg-1000 II/mark-III/master system/master system II/game gear/mega drive / genesis): Choose which system is going to be emulated.
- **System region (restart)** (**auto**/ntsc-u/pal/ntsc-j): Choose which region the system is from.  
- **System lookups** (**enabled**/disabled): Emulate system lockups 
- **System bootrom** (enabled/**disabled**): -
- **CD System BRAM** (**per bios**/per game ): -
- **68k address error** (**enabled**/disabled): Emulate the 68k address error.
- **Cartridge lock-on (restart)** (**disabled**/game genie/action replay (pro)/sonic & knuckles): Select lock-on cartridge.   
- **Master System FM** (**auto**/disabled/enabled): Enable the Master System FM chip.
- **YM2612 DAC quantization** (enabled/**disabled**): Enable YM2612 DAC quantization
- **8Blargg NTSC filter** (**disabled**/monochrome/composite/svidio/rgb): Enable Blargg NTSC filters.  
- **LCD Ghosting filter** (enabled/**disabled**): - 
- **Borders** (**disabled**/ top/bottom/ left/right / full): Enable borders.  
- **Game Gear extended screen** (enabled/**disabled**: Extend the Game Gear screen.
- **Core-provided aspect ratio** (**auto**/NTSC PAR/PAL PAR ): - 
- **Interlaced mode 2 output** (**single field**/double field): Change how interlaced mode 2 output is handled.   
- **Show Lightgun crosshair** (**no**/yes ): Self-explanatory. 
- **Invert Mouse Y-axis** (**no**/yes ): Self-explanatory. 

## Controllers

The Genesis Plus GX core supports fifteen different controller setting(s):

* Joypad Auto

![genesis_plus_gx_joypadauto](images/Controllers/genesis_plus_gx_joypad_auto.png)

* MD Joypad 3 Button

![genesis_plus_gx_mdjoypad3button](images/Controllers/genesis_plus_gx_mdjoypad3button.png)

* MD Joypad 6 Button

![genesis_plus_gx_mdjoypad6button](images/Controllers/genesis_plus_gx_mdjoybutton6button.png)

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

| Genesis GX Plus | Joypad Auto                                                    | MD Joypad 3 Button | MD Joypad 6 Button | MS Joypad 2 Button | MS Light Phaser | MS Paddle Control | MS Graphic Board | MS Sports Pad | MS XE-1AP | MD Mouse | 
|-----------------|----------------------------------------------------------------|--------------------|--------------------|--------------------|-----------------|-------------------|------------------|---------------|-----------|----------|                   
| B               | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               | -                  | -                  | -                  | -               | -                 | -                | -             | -         | -        |                                              
| A               | ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               | -                  | -                  | -                  | -               | -                 | -                | -             | -         | -        |
| Mode            | ![RetroPad_Select](images/RetroPad/Retro_Select.png)           | -                  | -                  | -                  | -               | -                 | -                | -             | -         | -        |
| Start           | ![RetroPad_Start](images/RetroPad/Retro_Start.png)             | -                  | -                  | -                  | -               | -                 | -                | -             | -         | -        |
| D-pad           | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)               | -                  | -                  | -                  | -               | -                 | -                | -             | -         | -        |
| C               | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               | -                  | -                  | -                  | -               | -                 | -                | -             | -         | -        |
| Y               | ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               | -                  | -                  | -                  | -               | -                 | -                | -             | -         | -        |
| X               | ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   | -                  | -                  | -                  | -               | -                 | -                | -             | -         | -        |
| Z               | ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   | -                  | -                  | -                  | -               | -                 | -                | -             | -         | -        |
|                 | ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              | -                  | -                  | -                  | -               | -                 | -                | -             | -         | -        |
|                 | ![RetroPad_R2](images/RetroPad/Retro_R2.png)                   | -                  | -                  | -                  | -               | -                 | -                | -             | -         | -        |
|                 | ![RetroPad_L3](images/RetroPad/Retro_L3.png)                   | -                  | -                  | -                  | -               | -                 | -                | -             | -         | -        |
|                 | ![RetroPad_R3](images/RetroPad/Retro_R3.png)                   | -                  | -                  | -                  | -               | -                 | -                | -             | -         | -        |
|                 | ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)   | -                  | -                  | -                  | -               | -                 | -                | -             | -         | -        |
|                 | ![RetroPad_Right_Stick](images/RetroPad/Retro_Right_Stick.png) | -                  | -                  | -                  | -               | -                 | -                | -             | -         | -        |


## Compatibility

100% compatibility with Genesis / Mega Drive, Sega/Mega CD, Master System, Game Gear & SG-1000 released software (including all unlicensed or pirate known dumps), also emulating backwards compatibility modes when available.

## External Links

* [Libretro Repository](https://github.com/libretro/Genesis-Plus-GX)
* [Report Libretro Issues Here](https://github.com/libretro/libretro-meta/issues)
* [Official Website](https://github.com/ekeeke/Genesis-Plus-GX)
