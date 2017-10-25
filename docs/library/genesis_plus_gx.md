# Sega MS/GG/MD/CD (Genesis Plus GX)

## Background

Genesis Plus GX is an open-source Sega 8/16 bit emulator focused on accuracy and portability. The source code, originally based on Genesis Plus 1.3 by Charles MacDonald, has been heavily modified & enhanced, with respect to initial goals and design, in order to improve the accuracy of emulation, implementing new features and adding support for extra peripherals, cartridge & systems hardware.

### Why use this core?

-

### Author(s): 

Charles McDonald|Eke-Eke

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/blob/master/docs/library/genesis_plus_gx.md). Changes are proposed using "Pull Requests."

## See also

-

## License

Non-commercial

## Extensions

*Content that can be loaded by the Genesis Plus GX core have the following file extensions*

mdx|md|smd|gen|bin|cue|iso|sms|gg|sg|68k|chd

## Database(s)

*RetroArch databases that are associated with the Genesis Plus GX core*

* Sega - Game Gear

* Sega - Master System - Mark III

* Sega - Mega-CD - Sega CD

* Sega - Mega Drive - Genesis

* Sega - PICO

* Sega - SG-1000

## BIOS

*Required or optional firmware files go in RetroArch's system directory.*

**Firmware files labelled (bootrom) and (lock-on) must have their corresponding core options enabled in order for them to be loaded.**

|   Filename    |    Description                         |              md5sum                     |
|:-------------:|:--------------------------------------:|:---------------------------------------:|
| bios_MD.bin   | [MegaDrive TMSS startup ROM (bootrom)](http://segaretro.org/TradeMark_Security_System) - Optional  | 45e298905a08f9cfb38fd504cd6dbc84 |
| bios_CD_E.bin | MegaCD EU BIOS - Required for EU       | e66fa1dc5820d254611fdcdba0662372        |
| bios_CD_U.bin | SegaCD US BIOS - Required for US       | 854b9150240a198070150e4566ae1290        |
| bios_CD_J.bin | MegaCD JP BIOS - Required for JP       | 278a9397d192149e84e820ac621a8edd        |
| bios_E.sms    | MasterSystem EU BIOS (bootrom) - Optional        | -                                       |
| bios_U.sms    | MasterSystem US BIOS (bootrom) - Optional        | -                                       |
| bios_J.sms    | MasterSystem JP BIOS (bootrom) - Optional        | -                                       |
| bios.gg       | GameGear BIOS (bootrom) - Optional               | -                                       |
| sk.bin        | Sonic & Knuckles ROM (lock-on) - Optional        | 4ea493ea4e9f6c9ebfccbdb15110367e        |
| sk2chip.bin   | Sonic & Knuckles UPMEM ROM (lock-on) - Optional  | b4e76e416b887f4e7413ba76fa735f16        |
| areplay.bin   | Action Replay ROM (lock-on) - Optional           | -                                       |
| ggenie.bin    | Game Genie ROM (lock-on) - Optional              | -                                       |

## Features

| Feature           | Supported |
|-------------------|:---------:|
| Saves             | ✔         |
| States            | ✔         |
| Rewind            | ✔         |
| Netplay           | ✔         |
| RetroAchievements | ✔         |
| RetroArch Cheats  | ✔         |
| Native Cheats     | ✕         |
| Controllers       | ✔         |
| Multi-Mouse       | ✕         |
| Rumble            | ✕         |
| Sensors           | ✕         |
| Camera            | ✕         |
| Location          | ✕         |
| Subsystem         | ✕         |

The Genesis Plus GX core creates directories named 'Genesis Plus GX' in RetroArch's...

* Savefile directory when the core is loaded.
* Statestate directory when the core is loaded.
* Config directory when a Core Override or a Game Override or a Game-options file is saved.
* Input Remapping directory when a Core Remap or a Game Remap is saved.
* Shaders Presets directory when a Core Preset or a Game Preset is saved.

Core Overrides/Remaps/Presets that are saved will be named 'Genesis Plus GX'.

Game Overrides/Remaps/Presets and Game-option files will have the same name as the loaded content.

Game data is saved/loaded to and from the core's save directory.

Save states are saved/loaded to and from the core's state directory. 

## Options

*The Genesis Plus GX core has the following options that can be tweaked from the core options menu. The default setting is bolded.*

- **System hardware (restart)** (**auto**/sg-1000/sg-1000 II/mark-III/master system/master system II/game gear/mega drive / genesis): Choose which system is going to be emulated.
- **System region (restart)** (**auto**/ntsc-u/pal/ntsc-j): Choose which region the system is from.
- **System lockups** (**On**/Off): Emulate system lockups that occur on real hardware.
- **System bootrom** (On/**Off**): - Runs BIOS if available and then starts loaded content after the boot sequence. The appropriate bootrom files must be in RetroArch's system directory.
- **CD System BRAM** (**per bios**/per game): The Sega CD's internal memory cannot hold a lot of saves. Setting this option to per game allows each game to have its own one brm file, thus negating any lack of available space issues.
- **68k address error** (**On**/Off): Emulate the [68k](http://segaretro.org/M68000) address error that occurs on real hardware. Set this to off when playing rom hacks since most emulators used to develop rom hacks don't emulate the error.
- **Cartridge lock-on (restart)** (**Off**/game genie/action replay (pro)/sonic & knuckles): Select lock-on cartridge. The appropriate lock-on cartride files must be in RetroArch's system directory.
- **Master System FM** (**auto**/Off/On): Enable the Master System FM chip. (Enhanced sound output support for [SMS compatible games](http://segaretro.org/FM_Sound_Unit_))
- **YM2612 DAC quantization** (On/**Off**): Enable YM2612 DAC quantization.
- **YM2612/YM3438 core** (**mame**/nuked (ym2612)/nuked (asic ym3438)/nuked (discrete ym3438):
- **Sound output** (**stereo**/mono): - 
- **Audio filter** (**Off**/low-pass): -
- **Low-pass filter %** (**60**/65/70/75/80/85/90/95/5/10/15/20/25/30/35/40/45/50/55): -
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

- **Core-provided aspect ratio** (**auto**/NTSC PAR/PAL PAR ): RetroArch's aspect ratio must be set to Core provided in the Video settings for this to function properly.

- **Interlaced mode 2 output** (**single field**/double field): Change how interlaced mode 2 output is handled. Games like Sonic 2's multiplayer mode uses Interlaced Mode 2.

??? note "*Interlaced mode 2 output - single field*"
    ![interlaced_mode_2_output_single_field](images\Cores\genesis_plus_gx\interlaced_mode_2_output_single_field.png)
	
??? note "*Interlaced mode 2 output - double field*"
    ![interlaced_mode_2_output_double_field](images\Cores\genesis_plus_gx\interlaced_mode_2_output_double_field.png)	

- **Show Lightgun crosshair** (**Off**/On ): Shows lightgun crosshairs for the MD Menancer, MD Justifiers, and MS Light Phaser device types.

??? note "*Lightgun crosshair*"
    ![lightgun_crosshair](images\Cores\genesis_plus_gx\lightgun_crosshair.png)

- **Invert Mouse Y-axis** (**Off**/On): For the MD Mouse Device Type

- **CPU speed** (**100%**/125%/150%/175%/200%): -

- **Remove per-line sprite limit** (**Off**/On): -

## Controllers

*The Genesis Plus GX core supports the following controller setting(s), bolded controller settings are the default for the specified user(s):*

### User 1 Device Type(s)

* **Joypad Auto** - Joypad without analog - Depending on the loaded content, the core will automatically emulate a MD Joypad 3 Button controller, or a MD Joypad 6 Button controller or a MS Joypad 2 Button controller*

* MD Joypad 3 Button - Joypad without analog 

* MD Joypad 6 Button - Joypad without analog

* MS Joypad 2 Button - Joypad without analog - also used for Game Gear

* MD Joypad 3 Button + 4-WayPlay - Joypad without analog - allows for up to four players to play together in certain games

* MD Joypad 6 Button + 4-WayPlay - Joypad without analog - allows for up to four players to play together in certain games

* MD Joypad 3 Button + Teamplayer - Joypad without analog - allows for up to four players to play together in certain games

* MD Joypad 6 Button + Teamplayer - Joypad without analog - allows for up to four players to play together in certain games

* MS Joypad 2 Button + Master Tap - Joypad without analog - allows for up to four players to play together in certain games

* MS Light Phaser - Lightgun

* MS Paddle Control - Joypad with analog

* MS Sports Pad - Joypad with analog

* MS Graphic Board - Pointer

* MD XE-1AP - Joypad with analog

* MD Mouse - Mouse

### User 2 Device Type(s)

* **Joypad Auto** - Joypad without analog - Depending on the loaded content, the core will automatically emulate a MD Joypad 3 Button controller, or a MD Joypad 6 Button controller or a MS Joypad 2 Button controller*

* MD Joypad 3 Button - Joypad without analog

* MD Joypad 6 Button - Joypad without analog

* MS Joypad 2 Button - Joypad without analog - also used for Game Gear

* MD Joypad 3 Button + 4-WayPlay - Joypad without analog - allows for up to four players to play together in certain games

* MD Joypad 6 Button + 4-WayPlay - Joypad without analog - allows for up to four players to play together in certain games

* MD Joypad 3 Button + Teamplayer - Joypad without analog - allows for up to four players to play together in certain games

* MD Joypad 6 Button + Teamplayer - Joypad without analog - allows for up to four players to play together in certain games

* MS Joypad 2 Button + Master Tap - Joypad without analog - allows for up to four players to play together in certain games

* MD Menancer - Lightgun

* MD Justifiers  - Lightgun

* MS Light Phaser - Lightgun

* MS Paddle Control - Joypad with analog

* MS Sports Pad - Joypad with analog

* MS Graphic Board - Pointer

* MD XE-1AP - Joypad with analog

* MD Mouse - Mouse

### User 3 - 16 Device Type(s)

* **RetroPad** - Joypad without analog

### Controllers graph

| Genesis Plus GX  | RetroPad                                                       | *MD Joypad 3 Button (+ 4-WayPlay) (+ Teamplayer)* | *MD Joypad 6 Button (+ 4-WayPlay) (+ Teamplayer)* | *MS Joypad 2 Button (+ Master Tap)* | *MS Paddle Control* | *MS Sports Pad* | *MD XE-1AP* |
|------------------|----------------------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------------------|---------------------|-----------------|-------------|
| B                | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               | B                                                 | B                                                 | 1                                   | 1                   | 1               | E2          |
| A                | ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               | A                                                 | A                                                 |                                     |                     |                 | E1          |
| Mode             | ![RetroPad_Select](images/RetroPad/Retro_Select.png)           |                                                   | Mode                                              |                                     |                     |                 | Select      |
| Start            | ![RetroPad_Start](images/RetroPad/Retro_Start.png)             | Start                                             | Start                                             | Start                               | Start               | Start           | Start       |
| D-pad            | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)               | D-pad                                             | D-pad                                             | D-pad                               |                     |                 |             |
| C                | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               | C                                                 | C                                                 | 2                                   |                     | 2               |             |
| Y                | ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               |                                                   | Y                                                 |                                     |                     |                 |             |
| X                | ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   |                                                   | X                                                 |                                     |                     |                 | C           |
| Y                | ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   |                                                   | Z                                                 |                                     |                     |                 | A           |
|                  | ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              |                                                   |                                                   |                                     |                     |                 | D           |
|                  | ![RetroPad_R2](images/RetroPad/Retro_R2.png)                   |                                                   |                                                   |                                     |                     |                 | B           |
|                  | ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)   |                                                   |                                                   |                                     | Paddle              | Trackball       | Thumb-stick |
|                  | ![RetroPad_Right_Stick](images/RetroPad/Retro_Right_Stick.png) |                                                   |                                                   |                                     |                     |                 | Slider      |

| RetroMouse                                                      | *Menacer* | *Justifiers* | *Light Phaser* | *Graphic Board* | *MD Mouse* |
|-----------------------------------------------------------------|-----------|--------------|----------------|-----------------|------------|
| ![Retro_Mouse](images/RetroMouse/Retro_Mouse.png)               | Pointer   | Pointer      | Pointer        | Pointer         | Pointer    | 
| ![RetroP_Left](images/RetroMouse/Retro_Left.png)                | A         | A            | A              | Pen             | Left       |
| Mouse wheel down                                                |           |              |                |                 | Center     |
| ![Retro_Middle](images/RetroMouse/Retro_Middle.png)             |           |              |                | Do              | Start      |
| ![Retro_Right](images/RetroMouse/Retro_Right.png)               | B         | B            | B              | Menu            | Right      |
| ![Retro_Left+Middle](images/RetroMouse/Retro_Left+Middle.png)   | C         | C            | C              |                 |            |
| ![Retro_Right+Middle](images/RetroMouse/Retro_Right+Middle.png) | Start     | Start        | Start          |                 |            |

## Compatibility

100% compatibility with Genesis / Mega Drive, Sega/Mega CD, Master System, Game Gear & SG-1000 released software (including all unlicensed or pirate known dumps), also emulating backwards compatibility modes when available.

## External Links

* [Libretro Repository](https://github.com/libretro/Genesis-Plus-GX)
* [Report Core Issues Here](https://github.com/libretro/libretro-meta/issues)
* [Official Website](https://github.com/ekeeke/Genesis-Plus-GX)
