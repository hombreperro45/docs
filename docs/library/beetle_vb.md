# Virtual Boy (Beetle VB)

## Background

Standalone port of Mednafen VB to libretro.

### Author(s):

Mednafen Team

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/beetle_vb.md). Changes are proposed using "Pull Requests."

## License

GPLv2

## Extensions

*Content that can be loaded by the Beetle VB core have the following file extensions.*

vb|vboy|bin

## Database(s)

*RetroArch databases that are associated with the Beetle VB core*

Nintendo - Virtual Boy

## BIOS

The Beetle VB core does not feature BIOS use.

## Features

| Feature           | Supported |
|-------------------|:---------:|
| Saves             | ✓         |
| States            | ✓         |
| Rewind            | ✓         |
| Netplay           | ✓         |
| RetroAchievements | ✕         |
| RetroArch Cheats  | ✕         |
| Native Cheats     | ✕         |
| Controllers       | ✓         |
| Multi-Mouse       | ✕         |
| Rumble            | ✕         |
| Sensors           | ✕         |
| Camera            | ✕         |
| Location          | ✕         |
| Subsystem         | ✕         |

The Beetle VB core creates directories named 'Mednafen VB' in RetroArch's...

* Savefile directory when the core is loaded.
* Statestate directory when the core is loaded.
* Config directory when a Core Override or a Game Override or a Game-options file is saved.
* Input Remapping directory when a Core Remap or a Game Remap is saved.
* Shaders Presets directory when a Core Preset or a Game Preset is saved.

Core Overrides/Remaps/Presets that are saved will be named 'Mednafen VB'.

Game Overrides/Remaps/Presets and Game-option files will have the same name as the loaded content.

Game data is saved/loaded to and from the core's save directory.

Save states are saved/loaded to and from the core's state directory.

## Options

*The Beetle VB core has the following option(s) that can be tweaked from the core options menu. The default setting is bolded.*

- **Anaglyph preset (restart)** (**Off**/red & blue/red & cyan/red & electric cyan/red & green/green & magenta/yellow & blue): Select anaglyph 3D mode.

**These Analglyph preset screenshots have been taken with the Palette core option set to black & red**

??? note "Anaglyph preset - Off"
	![anagylph_preset_off](images\Cores\beetle_vb\anagylph_preset_off.png)
	
??? note "Anaglyph preset - red & blue"
	![anagylph_preset_red&blue](images\Cores\beetle_vb\anagylph_preset_red&blue.png)

??? note "Anaglyph preset - red & cyan"
	![anagylph_preset_red&cyan](images\Cores\beetle_vb\anagylph_preset_red&cyan.png)

??? note "Anaglyph preset - red & electric cyan"
	![anagylph_preset_red&electriccyan](images\Cores\beetle_vb\anagylph_preset_red&electriccyan.png)

??? note "Anaglyph preset - red & green"
	![anagylph_preset_red&green](images\Cores\beetle_vb\anagylph_preset_red&green.png)

??? note "Anaglyph preset - green & magenta"
	![anagylph_preset_green&magenta](images\Cores\beetle_vb\anagylph_preset_green&magenta.png)

??? note "Anaglyph preset - yellow & blue"
	![anagylph_preset_yellow&blue](images\Cores\beetle_vb\anagylph_preset_yellow&blue.png)	

- **Palette (restart)** (**black & red**/black & white): Choose which color palette to use.

??? note "Palette - black & red"
	![palette_black&red](images\Cores\beetle_vb\palette_black&red.png)
	
??? note "Palette - black & white"
	![palette_black&white](images\Cores\beetle_vb\palette_black&white.png)
	
## Controllers

*The Beetle VB core supports the following controller setting(s), bolded controller settings are the default for the specified user(s):*

### User 1 - 16 Device Type(s)

* **RetroPad** - Joypad without analog

* RetroPad w/Analog - Joypad with analog

### Controllers graph

| Beetle VB         | RetroPad                                               |
|-------------------|--------------------------------------------------------|
| B                 | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)       |
| Select            | ![RetroPad_Select](images/RetroPad/Retro_Select.png)   |
| Start             | ![RetroPad_Start](images/RetroPad/Retro_Start.png)     |
| Left D-Pad Up     | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Up.png)    |
| Left D-Pad Down   | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Down.png)  |
| Left D-Pad Left   | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Left.png)  |
| Left D-Pad Right  | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Right.png) |
| A                 | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)       |
| L                 | ![RetroPad_L1](images/RetroPad/Retro_L1.png)           |
| R                 | ![RetroPad_R1](images/RetroPad/Retro_R1.png)           |
| Right D-Pad Up    | ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)      |
| Right D-Pad Left  | ![RetroPad_R2](images/RetroPad/Retro_R2.png)           |
| Right D-Pad Down  | ![RetroPad_L3](images/RetroPad/Retro_L3.png)           |
| Right D-Pad Right | ![RetroPad_R3](images/RetroPad/Retro_R3.png)           |

## Compatibility

Please file bugs that are reproducible on **upstream standalone** on the [official forums](https://forum.fobby.net/index.php?t=thread&frm_id=3&).

## External Links

* [Libretro Repository](https://github.com/libretro/beetle-vb-libretro)
* [Report Core Issues Here](https://github.com/libretro/libretro-meta)
* [Official Website](http://mednafen.sourceforge.net/)
* [Official Upstream Downloads](https://mednafen.github.io/releases/)