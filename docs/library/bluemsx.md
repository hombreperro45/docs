# MSX/SVI/ColecoVision/SG-1000 (blueMSX)

## Background

blueMSX is a cycle accurate emulator that emulates all generations of MSX computers as well as SVI, ColecoVision and Sega SG-1000.

Author(s): Daniel Vik

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/bluemsx.md). Changes are proposed using "Pull Requests."

## License

GPLv2

## Extensions

rom|ri|mx1|mx2|col|dsk|cas|sg|sc

## BIOS

The blueMSX core requires the BIOS and media files from the full standalone emulator installation.

Copy the **Machines** & **Databases** folders, from an official blueMSX emulator installation, into your chosen RetroArch "System/BIOS" directory.

(link to blueMSX official website at bottom of page)

## Features

| Feature           | Supported |
|-------------------|:---------:|
| Saves             | -         |
| States            | ✕         |
| Rewind            | ✕         |
| Netplay           | ✕         |
| RetroAchievements | ✕         |
| RetroArch Cheats  | ✕         |
| Native Cheats     | ✕         |
| Controllers       | ✔         |
| Multi-Mouse       | ✕         |
| Rumble            | ✕         |
| Sensors           | ✕         |
| Camera            | ✕         |
| Location          | ✕         |
| Subsystem         | ✕         |

## Options

The blueMSX core has the following options that can be tweaked from the core options menu. The default setting is bolded.

- **Machine Type (Restart)** (**MSX**/MSXturboR/MSX2/MSX2+/SEGA-SG-1000/SEGA-SC-3000/SEGA-SF-7000/SVI-Spectravideo SVI-318/SVI-Spectravideo SVI-328/SVI-Spectravideo SVI-328 Mk2/ColecoVision/Coleco (SVI-Spectravideo SVI-603)): Select the machine type you would like the core to start in. 
- **Crop Overscan** (**Off**/On/MSX2): Forces cropping of overscanned frames

??? note "*Crop Overscan Off*"
    ![crop_overscan_off](images\Cores\bluemsx\crop_overscan_off.png)

??? note "*Crop Overscan On*"
    ![crop_overscan_on](images\Cores\bluemsx\crop_overscan_on.png)

??? note "*Crop Overscan MSX2*"
    ![crop_overscan_msx2](images\Cores\bluemsx\crop_overscan_msx2.png)

- **VDP Sync Type (Restart)** (**Auto**/50Hz/60Hz): Match the game/machine region frequency to avoid emulated speed issues
- **Sound YM2413 Enable (Restart)** (**Off**/On): Sound YM2413 enable
- **Cart Mapper Type (Restart)** (**Auto**/normal/mirrored/basic/0x4000/0xC000/ascii8/ascii8sram/ascii16/ascii16sram/ascii16nf/konami4/konami4nf/konami5/konamisynth/korean80/korean90/korean126/MegaFlashRomScc/MegaFlashRomSccPlus/msxdos2/scc/sccexpanded/sccmirrored/sccplus/snatcher/sdsnatcher/SegaBasic/SG1000/SG1000Castle/SG1000RamA/SG1000RamB/SC3000/): When a rom game or application is in the database, the emulator uses the databases to apply the correct mapper. If the sha1 value of a dump is not yet in the databases, it uses an automatic mapper detection system, but it can fail in some cases. In this situation, you can manually select the correct mapper.

## Controllers

The blueMSX core supports 3 controller setting(s):

* RetroPad

* RetroKeyboard

* RetroPad Keyboard Map

| blueMSX              | [RetroPad](RetroPad)                                           | RetroKeyboard | RetroPad Keyboard Map |
|----------------------|----------------------------------------------------------------|---------------|-----------------------|
| Button 2             | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               |               |                       |
| Button 3, Colec #2   | ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               |               |                       |
| Select, Coleco *     | ![RetroPad_Select](images/RetroPad/Retro_Select.png)           |               |                       |
| Start, Coleco #      | ![RetroPad_Start](images/RetroPad/Retro_Start.png)             |               |                       |
| Dpad                 | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)               |               |                       |
| Button 1             | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               |               |                       |
| Button 4, Coleco #1  | ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               |               |                       |
| Button 5, Coleco #4  | ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   |               |                       |
| Button 6, Coleco #3  | ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   |               |                       |
| Button 7, Coleco #6  | ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              |               |                       |
| Button 8, Coleco #5  | ![RetroPad_R2](images/RetroPad/Retro_R2.png)                   |               |                       |
| Button 9, Coleco #8  | ![RetroPad_L3](images/RetroPad/Retro_L3.png)                   |               |                       |
| Button 10, Coleco #7 | ![RetroPad_R3](images/RetroPad/Retro_R3.png)                   |               |                       |
|                      | ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)   |               |                       |
|                      | ![RetroPad_Right_Stick](images/RetroPad/Retro_Right_Stick.png) |               |                       |

!!! note
    Colecovision inputs for **0 & 9** are mapped to Keyboard 1 & 2 for Player 1, 3 & 4 for Player 2.

## Compatibility

Unknown

## External Links

* [Libretro Repository](https://github.com/libretro/blueMSX-libretro)
* [Report Core Issues Here](https://github.com/libretro/libretro-meta)
* [Official Website](http://bluemsx.com/)
* [Official SourceForge Repository](http://sourceforge.net/projects/bluemsx/)
