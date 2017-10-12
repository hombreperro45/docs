# Sega MS/GG/MD/CD (Genesis Plus GX)

## Background

Genesis Plus GX is an open-source Sega 8/16 bit emulator focused on accuracy and portability. The source code, originally based on Genesis Plus 1.3 by Charles MacDonald, has been heavily modified & enhanced, with respect to initial goals and design, in order to improve the accuracy of emulation, implementing new features and adding support for extra peripherals, cartridge & systems hardware.

Author(s): Charles McDonald|Eke-Eke

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/blob/master/docs/library/genesis_plus_gx.md). Changes are proposed using "Pull Requests."

## License

Non-commercial

## Extensions

mdx|md|smd|gen|bin|cue|iso|sms|gg|sg|68k|chd

## BIOS

|   Filename    |    Description                         |              md5sum                     |
|:-------------:|:--------------------------------------:|:---------------------------------------:|
| bios_CD_E.bin | MegaCD EU BIOS - Required for EU       | e66fa1dc5820d254611fdcdba0662372        |
| bios_CD_U.bin | SegaCD US BIOS - Required for US       | 854b9150240a198070150e4566ae1290        |
| bios_CD_J.bin | MegaCD JP BIOS - Required for JP       | 278a9397d192149e84e820ac621a8edd        |
| bios_E.sms    | MasterSystem EU BIOS - Optional        | -                                       |
| bios_U.sms    | MasterSystem US BIOS - Optional        | -                                       |
| bios_J.sms    | MasterSystem JP BIOS - Optional        | -                                       |
| bios.gg       | GameGear BIOS - Optional               | -                                       |
| sk.bin        | Sonic & Knuckles ROM - Optional        | 4ea493ea4e9f6c9ebfccbdb15110367e        |
| sk2chip.bin   | Sonic & Knuckles UPMEM ROM - Optional  | b4e76e416b887f4e7413ba76fa735f16        |
| areplay.bin   | Action Replay ROM - Optional           | -                                       |
| ggenie.bin    | Game Genie ROM - Optional              | -                                       |

## Features

| Saves | States      | Rewind | Netplay | RetroAchievements | RetroArch Cheats | Native Cheats |
|:-----:|:-----------:|:------:|:-------:|:-----------------:|:----------------:|:-------------:|
|  yes  |   yes       | yes    |  yes    |     yes           | yes              | no            |

| Controllers     | Rumble | Sensors | Camera | Location | Subsystem     |
|:---------------:|:------:|:-------:|:------:|:--------:|:-------------:|
|      yes        |  no    |   no    |  no    |   no     |      no       |

## Options

- **System hardware (restart)** (**auto**/sg-1000/sg-1000 II/mark-III/master system/master system II/game gear/mega drive / genesis): Choose which system is going to be emulated.
- **System region (restart)** (**auto**/ntsc-u/pal/ntsc-j): Choose which region the system is from.
- **System lookups** (**On**/Off): Emulate system lockups that occur on real hardware.
- **System bootrom** (On/**Off**): - Runs BIOS if available and then starts loaded content after the boot sequence
- **CD System BRAM** (**per bios**/per game): The Sega CD's internal memory cannot hold a lot of saves. Setting this option to per game allows each game to have its own one brm file, thus negating any lack of available space issues.
- **68k address error** (**On**/Off): Emulate the 68k address error that occurs on real hardware. Set this to off when playing rom hacks since most emulators used to develop rom hacks don't emulate the error.
- **Cartridge lock-on (restart)** (**Off**/game genie/action replay (pro)/sonic & knuckles): Select lock-on cartridge. The appropriate lock-on cartride files must be in RetroArch's system directory.
- **Master System FM** (**auto**/Off/On): Enable the Master System FM chip. (Enhanced sound output support for [SMS compatible games](http://segaretro.org/FM_Sound_Unit_))
- **YM2612 DAC quantization** (On/**Off**): Enable YM2612 DAC quantization.
- **YM2612/YM3438 core** (**mame**/nuked opn2): 
- **Audio filter** (**Off**/lowpass): -
- **Sound output** (**On**/Off): -
- **Low-pass filter %** (5-**60**-95): -
- **Blargg NTSC filter** (**Off**/monochrome/composite/svidio/rgb): Enable Blargg NTSC filters.

??? note "*Blargg NTSC filter - Off*"
    ![blargg_ntsc_filter_disabled](images\Cores\genesis_plus_gx\blargg_ntsc_filter_disabled.png)

??? note "*Blargg NTSC filter  - monochrome*"
    ![blargg_ntsc_filter_monochrome](images\Cores\genesis_plus_gx\blargg_ntsc_filter_monochrome.png)

??? note "*Blargg NTSC filter - composite*"
    ![blargg_ntsc_filter_composite](images\Cores\genesis_plus_gx\blargg_ntsc_filter_composite.png)

??? note "*Blargg NTSC filter  - svideo*"
    ![blargg_ntsc_filter_svideo](images\Cores\genesis_plus_gx\blargg_ntsc_filter_svideo.png)

??? note "*Blargg NTSC filter - rgb*"
    ![blargg_ntsc_filter_rgb](images\Cores\genesis_plus_gx\blargg_ntsc_filter_rgb.png)

- **LCD Ghosting filter** (On/**Off**): Enable LCD Gshoting filter

??? note "*LCD Ghosting filter - On*"
    ![lcd_ghosting_filter_on](images\Cores\genesis_plus_gx\lcd_ghosting_filter_on.png)

- **Borders** (**Off**/ top/bottom/ left/right / full): Enable borders.
- **Game Gear extended screen** (On/**Off**: Extend the Game Gear screen.

??? note "*Game Gear extended screen - Off*"
    ![game_gear_extended_screen_off](images\Cores\genesis_plus_gx\game_gear_extended_screen_off.png)

??? note "*Game Gear extended screen - On*"
    ![game_gear_extended_screen_on](images\Cores\genesis_plus_gx\game_gear_extended_screen_on.png)

- **Core-provided aspect ratio** (**auto**/NTSC PAR/PAL PAR ): RetroArch's aspect ratio must be set to Core provided for this to have any visible effect. 

- **Interlaced mode 2 output** (**single field**/double field): Change how interlaced mode 2 output is handled. Games like Sonic 2's multiplayer mode uses Interlaced Mode 2.

??? note "*Interlaced mode 2 output - single field*"
    ![interlaced_mode_2_output_single_field](images\Cores\genesis_plus_gx\interlaced_mode_2_output_single_field.png)
	
??? note "*Interlaced mode 2 output - double field*"
    ![interlaced_mode_2_output_double_field](images\Cores\genesis_plus_gx\interlaced_mode_2_output_double_field.png)	

- **Show Lightgun crosshair** (**Off**/On ): Shows lightgun crosshairs for the MD Menancer, MD Justifiers, and MS Light Phaser device types.

??? note "*Lightgun crosshair*"
    ![lightgun_crosshair](images\Cores\genesis_plus_gx\lightgun_crosshair.png)

- **Invert Mouse Y-axis** (**Off**/On ): For the MD Mouse Device Type

## Controllers

The Genesis Plus GX core supports seventeen different controller setting(s):

## User 1 and 2 Device Types

* **Joypad Auto** - Default [Joypad] *Depending on the loaded content, the core will automatically emulate a MD Joypad 3 Button controller, or a MD Joypad 6 Button controller or a MS Joypad 2 Button controller*

* **MD Joypad 3 Button** - [Joypad] 

* **MD Joypad 6 Button** - [Joypad] 

* **MS Joypad 2 Button** - [Joypad] *also used for Game Gear*

* **MD Joypad 3 Button + 4-WayPlay** - [Joypad] *allows for up to four players to play together in certain games*

* **MD Joypad 6 Button + 4-WayPlay** - [Joypad] *allows for up to four players to play together in certain games*

* **MD Joypad 3 Button + Teamplayer** - [Joypad] *allows for up to four players to play together in certain games*

* **MD Joypad 6 Button + Teamplayer** - [Joypad] *allows for up to four players to play together in certain games*

* **MS Joypad 2 Button + Master Tap** - [Joypad] *allows for up to four players to play together in certain games*

* **MS Light Phaser** - [Lightgun]

* **MS Paddle Control** - [Analog]

* **MS Graphic Board** - [Pointer]

* **MS Sports Pad** - [Analog]

* **MD XE-1AP** - [Analog]

* **MD Mouse** - [Mouse]

## User 2 Device Types

* **MD Menancer** - [Lightgun]

* **MD Justifiers**  - [Lightgun]

| Genesis Plus GX  | RetroPad                                                       | MD Joypad 3 Button | MD Joypad 6 Button | MS Joypad 2 Button | MS Paddle Control | MS Sports Pad | MD XE-1AP   |
|------------------|----------------------------------------------------------------|--------------------|--------------------|--------------------|-------------------|-------------- |-------------|
| B                | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               | B                  | B                  | 1                  | 1                 | 1             | E2          |
| A                | ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               | A                  | A                  |                    |                   |               | E1          |
| Mode             | ![RetroPad_Select](images/RetroPad/Retro_Select.png)           |                    | Mode               |                    |                   |               | Select      |
| Start            | ![RetroPad_Start](images/RetroPad/Retro_Start.png)             | Start              | Start              | Start              | Start             | Start         | Start       |
| D-pad            | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)               | D-pad              | D-pad              | D-pad              |                   |               |             |
| C                | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               | C                  | C                  | 2                  |                   | 2             |             |
| Y                | ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               |                    | Y                  |                    |                   |               |             |
| X                | ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   |                    | X                  |                    |                   |               | C           |
| Y                | ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   |                    | Z                  |                    |                   |               | A           |
|                  | ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              |                    |                    |                    |                   |               | D           |
|                  | ![RetroPad_R2](images/RetroPad/Retro_R2.png)                   |                    |                    |                    |                   |               | B           |
|                  | ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)   |                    |                    |                    | Paddle            | Trackball     | Thumb-stick |
|                  | ![RetroPad_Right_Stick](images/RetroPad/Retro_Right_Stick.png) |                    |                    |                    |                   |               | Slider      |

| RetroMouse                                                    | Menacer | Justifiers | Light Phaser | Graphic Board | MD Mouse |
|---------------------------------------------------------------|---------|------------|--------------|---------------|----------|
| ![Retro_Mouse](images/RetroMouse/Retro_Mouse.png)               | Pointer | Pointer    | Pointer      | Pointer       | Pointer  |
| ![RetroP_Left](images/RetroMouse/Retro_Left.png)                | A       | A          | A            | Pen           | Left     |
| Mouse wheel down                                              |         |            |              |               | Center   |
| ![Retro_Middle](images/RetroMouse/Retro_Middle.png)             |         |            |              | Do            | Start    |
| ![Retro_Right](images/RetroMouse/Retro_Right.png)               | B       | B          | B            | Menu          | Right    |
| ![Retro_Left+Middle](images/RetroMouse/Retro_Left+Middle.png)   | C       | C          | C            |               |          |
| ![Retro_Right+Middle](images/RetroMouse/Retro_Right+Middle.png) | Start   | Start      | Start        |               |          |

## Compatibility

100% compatibility with Genesis / Mega Drive, Sega/Mega CD, Master System, Game Gear & SG-1000 released software (including all unlicensed or pirate known dumps), also emulating backwards compatibility modes when available.

## External Links

* [Libretro Repository](https://github.com/libretro/Genesis-Plus-GX)
* [Report Core Issues Here](https://github.com/libretro/libretro-meta/issues)
* [Official Website](https://github.com/ekeeke/Genesis-Plus-GX)
