# Sega MS/MD/CD/32X (PicoDrive)

## Background

PicoDrive is an open-source Sega 8/16 bit and 32X emulator which was written having ARM-based handheld devices in mind.

### Why use this core?

* Only libretro core that supports 32x emulation.

* If your preferred device is too weak to run any other cores.

### Author(s):

notaz|fdave

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/picodrive.md). Changes are proposed using "Pull Requests."

## See also

[Genesis Plus GX](https://buildbot.libretro.com/docs/library/genesis_plus_gx/)

## License

MAME

## Extensions

*Content that can be loaded by the PicoDrive core have the following file extensions.*

bin|gen|smd|md|32x|cue|iso|sms|68k

## Database(s)

*RetroArch databases that are associated with the PicoDrive core*

* Sega - Master System - Mark III
* Sega - Mega Drive - Genesis
* Sega - PICO
* Sega - 32X

## BIOS

*Required or optional firmware files go in RetroArch's system directory.*

|   Filename     |    Description             |              md5sum             |
|:--------------:|:--------------------------:|:-------------------------------:|
| bios_CD_E.bin  | MegaCD EU BIOS - Required | e66fa1dc5820d254611fdcdba0662372 |
| bios_CD_U.bin  | SegaCD US BIOS - Required | 2efd74e3232ff260e371b99f84024f7f |
| bios_CD_J.bin  | MegaCD JP BIOS - Required | 278a9397d192149e84e820ac621a8edd |

## Features

| Feature           | Supported |
|-------------------|:---------:|
| Saves             | ✓         |
| States            | ✓         |
| Rewind            | ✓         |
| Netplay           | ✓         |
| RetroAchievements | -         |
| RetroArch Cheats  | -         |
| Native Cheats     | ✕         |
| Controllers       | ✓         |
| Multi-Mouse       | ✕         |
| Rumble            | ✕         |
| Sensors           | ✕         |
| Camera            | ✕         |
| Location          | ✕         |
| Subsystem         | ✕         |

The PicoDrive core creates directories named 'PicoDrive' in RetroArch's...

* Savefile directory when the core is loaded.
* Statestate directory when the core is loaded.
* Config directory when a Core Override or a Game Override or a Game-options file is saved.
* Input Remapping directory when a Core Remap or a Game Remap is saved.
* Shaders Presets directory when a Core Preset or a Game Preset is saved.

Core Overrides/Remaps/Presets that are saved will be named 'PicoDrive'.

Game Overrides/Remaps/Presets and Game-option files will have the same name as the loaded content.

Game data is saved/loaded to and from the core's save directory.

Save states are saved/loaded to and from the core's state directory.

## Options

*The PicoDrive core has the following option(s) that can be tweaked from the core options menu. The default setting is bolded.*

- **Input device 1** (**3 button pad**/6 button pad/None): Choose which kind of controller is plugged in slot 1.
- **Input device 2** (**3 button pad**/6 button pad/None): Choose which kind of controller is plugged in slot 2.
- **No sprite limit** (**Off**/On): Enable this to remove the sprite limit.
- **MegaCD RAM cart** (**Off**/On): Emulate a MegaCD RAM cart.
- **Region** (**Auto**/Japan NTSC/Japan PAL/US/Europe): Force a specific region.

- **Core-provided aspect ratio** (**PAR**/ 4/3 /CRT): Choose the core-provided aspect ratio. RetroArch's aspect ratio must be set to Core provided in the Video seetings. 

??? note "Core-provided aspect ratio - PAR"
	![PAR](images\Cores\picodrive\PAR.png)
	
??? note "Core-provided aspect ratio - 4/3"
	![4by3](images\Cores\picodrive\4by3.png)
	
??? note "Core-provided aspect ratio - CRT"
	![CRT](images\Cores\picodrive\CRT.png)

- **Show Overscan** (**Off**/On): Crop out the potentially random glitchy video output that would have been hidden by the bezel around the edge of a standard-definition television screen.

??? note "Show Overscan - Off"
	![overscan_disabled](images\Cores\picodrive\overscan_disabled.png)
	
??? note "Show Overscan - On"
	![overscan_enabled](images\Cores\picodrive\overscan_enabled.png)

- **68k overclock** (**Off**/+25%/+50%/+75%/+100%/+200%/+400%): Overclock the emulated [68k chip](http://segaretro.org/M68000)
- **Dynamic recompilers** (Off/**On**): Use dynamic recompilers **(this core option is not available on all hardware)**.

## Controllers

*The PicoDrive core supports the following controller setting(s), bolded controller settings are the default for the specified user(s):*

### User 1 - 16 Device Type(s)

* **RetroPad** - Joypad without analog

* RetroPad w/Analog - Joypad with analog

### Controllers graph

| PicoDrive   | RetroPad                                                       |
|-------------|----------------------------------------------------------------|
| B           | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               |
| A           | ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               |
| Mode        | ![RetroPad_Select](images/RetroPad/Retro_Select.png)           |
| Start       | ![RetroPad_Start](images/RetroPad/Retro_Start.png)             |
| D-Pad Up    | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Up.png)            |
| D-Pad Down  | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Down.png)          |
| D-Pad Left  | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Left.png)          |
| D-Pad Right | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Right.png)         |
| C           | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               |
| Y           | ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               |
| X           | ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   |
| Z           | ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   |

## Compatibility

| 32x Games                                    | Issue                                                         |
|----------------------------------------------|---------------------------------------------------------------|
| Brutal Unleashed – Above the Claw            | Softlocks after the first fight.                              |
| FIFA Soccer ’96                              | Glitched main menu text.                                      |
| Knuckles’ Chaotix                            | Glitched graphics on the Player Select screen.                |
| NBA Jam Tournament Edition                   | Framerate issues.                                             |
| NFL Quarterback Club                         | Some menu graphics are missing.                               |
| Star Wars Arcade (PAL version)               | Glitched opening visuals. Cannot get past Press Start screen. | 
| Virtua Racing Deluxe                         | Blinking line during the SEGA logo screen.                    |
| World Series Baseball Starring Deion Sanders | Crashes when starting a match.                                |
| WWF Raw                                      | Various graphics are missing.                                 | 

## External Links

* [Libretro Repository](https://github.com/libretro/picodrive)
* [Report Core Issues Here](https://github.com/libretro/libretro-meta)
* [Official Website](http://notaz.gp2x.de/pico.php)
* [Official Repository](https://github.com/notaz/picodrive)