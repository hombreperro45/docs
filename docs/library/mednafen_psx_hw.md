# PlayStation (Beetle PSX HW)

## Background

Enhanced port of standalone Mednafen PSX to libretro. 

Authors: Mednafen Team | Retroarch Team

## License

GPLv2

## Extensions

cue|toc|m3u|ccd|exe|pbp

## BIOS

Beetle-PSX HW requires the following BIOS image files for operation

|   Filename    |    Description     |              md5sum              |
|:-------------:|:------------------:|:--------------------------------:|
|scph5500.bin   |PS1 JP BIOS         |8dd7d5296a650fac7319bce665a6a53c  |
|scph5501.bin   |PS1 US BIOS         |490f666e1afb15b7362b406ed1cea246  |
|scph5502.bin   |PS1 EU BIOS         |32736f17079d0b2b7024407c39bd3050  |


## Feature Support
These are libretro features, not frontend or standalone emulator features.

##### Features:
| Saves | States | Rewind | Netplay | RetroAchievements | Cheats | Controllers |
|-------|--------|--------|---------|-------------------|--------|-------------|
| yes   | yes    |  yes   |  yes    |        no         |  yes   |    yes      |

| Rumble | Sensors | Camera | Location | Subsystem |
|--------|---------|--------|----------|-----------|
|  yes   |    no   |  no    |    no    |    no     |

## Running

To run this core, the "system directory" must be defined if running in RetroArch. The PSX BIOS must be placed there, $sysdir/scph550{0,1,2} for Japanese, NA and EU regions respectively.

Memory cards will be saved to "save directory", memory card slot 0 is saved using libretro's standard interface. The rest of memory cards are saved using Mednafen's standard mechanism. You might have to rename your old memory cards to gamename.srm. Alternatively you may just rename it from gamename.gamenamehash.0.mcr to gamename.gamenamehash.1.mcr and load them off the corresponding slot.

## Loading ISOs

Beetle differs from other PS1 emulators in that it needs a cue-sheets that points to an image file, usually an .iso/.bin file. If you have e.g. foo.iso, you should create a foo.cue, and fill this in:

FILE "foo.iso" BINARY
   TRACK 01 MODE1/2352
      INDEX 01 00:00:00

After that, you can load the foo.cue file as a ROM. Note that this is a dirty hack and will not work on all games. Ideally, make sure to use rips that have cue-sheets.

If foo is a multiple-disk game, you should have .cue files for each one, e.g. foo (Disc 1).cue, foo (Disc 2).cue, foo (Disc 3).cue.To take advantage of Beetle's Disk Control feature for disk swapping, an index file should be made.

Open a text file and enter your game's .cue files on it, like this:

foo (Disc 1).cue
foo (Disc 2).cue
foo (Disc 3).cue

Save as foo.m3u and use this file in place of each disk's individual cue sheet.

## Condensing Games

Alternatively to using cue sheets with .bin/.iso files, you can convert your games to .pbp (Playstation Portable update file) to reduce file sizes and neaten up your game folder. If converting a multiple-disk game, all disks should be added to the same .pbp file, rather than making a .m3u file for them.

Most conversion tools will want a single .bin/.iso file for each disk. If your game uses multiple .bin files (tracks) per disk, you will have to mount the cue sheet to a virtual drive and re-burn the images onto a single track before conversion.

Note that RetroArch does not currently have .pbp database due to variability in users' conversion methods. All .pbp games will have to be added to playlists manually.

## Options
|   Core Option                     |         Description         | Options (Default Bolded)                   | Requires Restart |
|:---------------------------------:|:---------------------------:|:------------------------------------------:|:----------------:|
|Renderer                           | Renderer backend - The last two options will enable and/or speedup enhancements like upscaling and texture filtering. † | software/**vulkan**/opengl | yes |
|Software framebuffer               | If off, the software renderer will skip some steps. Potential speedup. Causes bad graphics when doing framebuffer readbacks. | Off/**On** | - |
|Adaptive smoothing                 | When upscaling, smooths out 2D elements while keeping 3D elements sharp. Vulkan renderer only at the moment. | Off/**On** | - |
|Internal GPU Resolution            | Graphics upscaling. | **1x(native)**/2x/4x/8x/16x/32x | - |
|Texture filtering                  | Per-texture filtering. OpenGL only at the moment. | **nearest**/SABR/xBR/bilinear/3-point/JINC2 | - |
|Internal color depth               | PSX had 16bpp depth, beetle-psx can go up to 32bpp. OpenGL only at the moment. Vulkan always uses 32bpp. | **dithered 16bpp (native)**/32bpp | - |
|Wireframe mode                     | For debug use. Shows only the outlines of polygons. OpenGL only. | **Off**/On | - |
|Display full VRAM                  | Everything in VRAM is drawn on screen. | **Off**/On | - |
|PGXP operation mode                | When not off, floating point coordinates will be used for vertex positions, to avoid the PSX polygon jitter. 'memory + cpu' mode can further reduce jitter at the cost of performance and geometry glitches. | **Off**/memory only/memory + cpu | - |
|PGXP vertex cache                  | Maintains a cache for vertices. May result in better performance but can result in graphics glitches in most games. | **Off**/On | - |
|PGXP perspective correct texturing | Original PSX did affine texture mapping, resulting in e.g. crooked lines across walls. This fixes it. | **Off**/On | - |
|Widescreen mode hack               | If on, renders in 16:9. Works best on 3D games. | **Off**/On | no |
|Frame duping (speedup)             | Redraws/reuses the last frame if there was no new data. | **Off**/On | - |
|CPU Overclock                      | Gets rid of memory access latency and makes all GTE instructions have 1 cycle latency. | **Off**/On | - |
|Skip BIOS                          | Self-explanatory. Some games have issues when enabled. | **Off**/On  | - |
|Dithering pattern                  | If off, disables the dithering pattern the PSX applies to combat color banding. OpenGL only. Vulkan always disables the pattern. | **1x(native)**/internal resolution/Off | - |
|Display internal FPS               | Shows the frame rate at which the emulated PSX is drawing at. Onscreen Notifications must be enabled in the Retroarch Onscreen Display Settings. | **Off**/On | - |
|Initial scanline                   | Sets the first scanline to be drawn on screen. | **0** - 40 | - |
|Last scanline                      | Sets the last scanline to be drawn on screen. | 210 - **239** | - |
|Initial scanline PAL               | Sets the first scanline to be drawn on screen for PAL systems. | **0** - 40 | - |
|Last scanline PAL                  | Sets the last scanline to be drawn on screen for PAL systems. | 260 - **287** | - |
|Crop Overscan                      | Self-explanatory. | Off/**On** | - |
|Additional Cropping                | Self-explanatory. | **Off**/1 px - 8 px | - |
|Offset Cropped Image               | Self-explanatory. | -4 px - -1 px /**Off**/ 1 px - 4 px | - |
|Analog self-calibration            | Monitors the max values reached by the input, using it as a calibration heuristic which then scales the analog coordinates sent to the emulator accordingly. For best results, rotate the sticks at max amplitude for the algorithm to get a good estimate of the scaling factor, otherwise it will adjust while playing | **Off**/On | - |
|DualShock Analog button toggle     | Toggles the Analog button from DualShock controllers, if disabled analogs are always on, if enabled you can toggle their state by pressing and holding START+SELECT+L1+L2+R1+R2. | **Off**/On | - |
|Port 1: Multitap enable            | Enables/Disables multitap functionality on port 1. | **Off**/On | - |
|Port 2: Multitap enable            | Enables/Disables multitap functionality on port 2. | **Off**/On | - |
|CD Image Cache                     | Loads the complete image in memory at startup. | **Off**/On | yes |
|Memcard 0 method                   | Picks the format (libretro or mednafen) used for storing memcard 0 save data. | **libretro**/mednafen | - |
|Enable memory card 1               | Specifically enables memcard slot 1. Needed for game "Codename Tenka". | Off/**On** | - |
|Shared memcards                    | Stores everything in the same savefile. 'Memcard 0 method' needs to be set to 'libretro'. | **Off**/On | yes |

† The Software renderer can be used with any Video Driver. The opengl renderer must be used with the gl Video Driver and the vulkan renderer must be used with the vulkan Video Driver. Retroarch's Video Driver can be changed in the Retroarch Driver settings.

## Controllers

This core supports four controllers: 

![ps1_joypad_diagram](images/Controllers/ps1_joypad.png)

* PS1 Joypad: PlayStation Controller (SCPH-1080)


* DualAnalog: PlayStation Dual Analog Controller(SCPH-1180)


* DualShock: DualShock (SCPH-1200)


* FlightStick: PlayStation Analog Joystick (SCPH-1110)


| [RetroPad](RetroPad)                                           | PS1 Joypad                                               | DualAnalog                                                     | DualShock                                                      | FlightStick                                                    |
|----------------------------------------------------------------|----------------------------------------------------------|----------------------------------------------------------------|----------------------------------------------------------------|----------------------------------------------------------------|                                                                |                                                                |                                                          |                                                                |                                                                |                                                                |
| ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               | ![PS3_Circle](images/Button Pack/PS3/PS3_Circle.png)     | ![PS3_Circle](images/Button Pack/PS3/PS3_Circle.png)           | ![PS3_Circle](images/Button Pack/PS3/PS3_Circle.png)           | ![PS3_Circle](images/Button Pack/PS3/PS3_Circle.png)           |
| ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               | ![PS3_Cross](images/Button Pack/PS3/PS3_Cross.png)       | ![PS3_Cross](images/Button Pack/PS3/PS3_Cross.png)             | ![PS3_Cross](images/Button Pack/PS3/PS3_Cross.png)             | ![PS3_Cross](images/Button Pack/PS3/PS3_Cross.png)             |
| ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)               | ![PS3_Dpad](images/Button Pack/PS3/PS3_Dpad.png)         | ![PS3_Dpad](images/Button Pack/PS3/PS3_Dpad.png)               | ![PS3_Dpad](images/Button Pack/PS3/PS3_Dpad.png)               | ![PS3_Dpad](images/Button Pack/PS3/PS3_Dpad.png)               |
| ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   | ![PS3_L1](images/Button Pack/PS3/PS3_L1.png)             | ![PS3_L1](images/Button Pack/PS3/PS3_L1.png)                   | ![PS3_L1](images/Button Pack/PS3/PS3_L1.png)                   | ![PS3_L1](images/Button Pack/PS3/PS3_L1.png)                   |
| ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              | ![PS3_L2](images/Button Pack/PS3/PS3_L2.png)             | ![PS3_L2](images/Button Pack/PS3/PS3_L2.png)                   | ![PS3_L2](images/Button Pack/PS3/PS3_L2.png)                   | ![PS3_L2](images/Button Pack/PS3/PS3_L2.png)                   |
| ![RetroPad_L3](images/RetroPad/Retro_L3.png)                   |                                                          |                                                                | ![PS3_L3](images/Button Pack/PS3/PS3_L3.png)                   |                                                                |
| ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)   |                                                          | ![PS3_Left_Stick](images/Button Pack/PS3/PS3_Left_Stick.png)   | ![PS3_Left_Stick](images/Button Pack/PS3/PS3_Left_Stick.png)   | ![PS3_Left_Stick](images/Button Pack/PS3/PS3_Left_Stick.png)   |                                                        
| ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   | ![PS3_R1](images/Button Pack/PS3/PS3_R1.png)             | ![PS3_R1](images/Button Pack/PS3/PS3_R1.png)                   | ![PS3_R1](images/Button Pack/PS3/PS3_R1.png)                   | ![PS3_R1](images/Button Pack/PS3/PS3_R1.png)                   |
| ![RetroPad_R2](images/RetroPad/Retro_R2.png)                   | ![PS3_R2](images/Button Pack/PS3/PS3_R2.png)             | ![PS3_R2](images/Button Pack/PS3/PS3_R2.png)                   | ![PS3_R2](images/Button Pack/PS3/PS3_R2.png)                   | ![PS3_R2](images/Button Pack/PS3/PS3_R2.png)                   |
| ![RetroPad_R3](images/RetroPad/Retro_R3.png)                   |                                                          |                                                                | ![PS3_R3](images/Button Pack/PS3/PS3_R3.png)                   |                                                                |
| ![RetroPad_Right_Stick](images/RetroPad/Retro_Right_Stick.png) |                                                          | ![PS3_Right_Stick](images/Button Pack/PS3/PS3_Right_Stick.png) | ![PS3_Right_Stick](images/Button Pack/PS3/PS3_Right_Stick.png) | ![PS3_Right_Stick](images/Button Pack/PS3/PS3_Right_Stick.png) |
| ![RetroPad_Select](images/RetroPad/Retro_Select.png)           | ![PS3_Select](images/Button Pack/PS3/PS3_Select.png)     | ![PS3_Select](images/Button Pack/PS3/PS3_Select.png)           | ![PS3_Select](images/Button Pack/PS3/PS3_Select.png)           | ![PS3_Select](images/Button Pack/PS3/PS3_Select.png)           |
| ![RetroPad_Start](images/RetroPad/Retro_Start.png)             | ![PS3_Start](images/Button Pack/PS3/PS3_Start.png)       | ![PS3_Start](images/Button Pack/PS3/PS3_Start.png)             | ![PS3_Start](images/Button Pack/PS3/PS3_Start.png)             | [PS3_Start](images/Button Pack/PS3/PS3_Start.png)              |
| ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               | ![PS3_Triangle](images/Button Pack/PS3/PS3_Triangle.png) | ![PS3_Triangle](images/Button Pack/PS3/PS3_Triangle.png)       | ![PS3_Triangle](images/Button Pack/PS3/PS3_Triangle.png)       | ![PS3_Triangle](images/Button Pack/PS3/PS3_Triangle.png)       |
| ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               | ![PS3_Square](images/Button Pack/PS3/PS3_Square.png)     | ![PS3_Square](images/Button Pack/PS3/PS3_Square.png)           | ![PS3_Square](images/Button Pack/PS3/PS3_Square.png)           | ![PS3_Square](images/Button Pack/PS3/PS3_Square.png)           |

* The respective input device Controls setting must have Analog to Digital Type set to none for normal Analog operation.

* Rumble only works when device type is set to Dualshock

## External Links

* [Libretro Repository](https://github.com/libretro/beetle-psx-libretro)
* [Report Issues Here](https://github.com/libretro/beetle-psx-libretro/issues)
* [Official Standalone Website](https://mednafen.github.io/)
