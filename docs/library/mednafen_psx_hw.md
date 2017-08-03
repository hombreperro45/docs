# PlayStation (Beetle PSX HW)

## Background

Enhanced port of standalone Mednafen PSX to libretro. |Authors:- Mednafen Team|Retroarch Team

## License

GPLv2

## Extensions

cue|toc|m3u|ccd|exe|pbp

## BIOS

Beetle-PSX requires the following BIOS image files for operation

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
| yes   | yes    |  yes   |  yes    |         -         |  yes   |    yes      |

| Rumble | Sensors | Camera | Location | Subsystem |
|--------|---------|--------|----------|-----------|
|  yes   |    -    |  -     |    -     |     -     |

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
|Crop Overscan                      | - | Off/**On** | - |
|Additional Cropping                | - | **Off**/1 px - 8 px | - |
|Offset Cropped Image               | - | -4 px - -1 px /**Off**/ 1 px - 4 px | - |
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

The core supports these controller setting:
* Beetle PSX HW Joypad: PS1 Joypad
* Beetle PSX HW Joypad: DualAnalog
* Beetle PSX HW Joypad: DualShock
* Beetle PSX HW Joypad: FlightStick

| [RetroPad](RetroPad)                                           | Joypad |
|----------------------------------------------------------------|--------|
| ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               | Circle |
| ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               | Cross  |
| ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)               | D-Pad  |
| ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   | L      |
| ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              | L2     |
| ![RetroPad_L3](images/RetroPad/Retro_L3.png)                   | L3     |
| ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)   | Left Analog Stick |
| ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   | R      |
| ![RetroPad_R2](images/RetroPad/Retro_R2.png)                   | R2     |
| ![RetroPad_R3](images/RetroPad/Retro_R3.png)                   | R3     |
| ![RetroPad_Right_Stick](images/RetroPad/Retro_Right_Stick.png) | Right Analog Stick |
| ![RetroPad_Select](images/RetroPad/Retro_Select.png)           | Select |
| ![RetroPad_Start](images/RetroPad/Retro_Start.png)             | Start  |
| ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               | Triangle |
| ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               | Square |

* Analog Sticks only work when the device type is set to DualAnalog or DualShock. Also, the respective input device Controls setting must have Analog to Digital Type set to none.

* Rumble only works when device type is set to Dualshock

## External Links

* [Official Website](https://mednafen.github.io/)
* [Libretro Repository](https://github.com/libretro/beetle-psx-libretro)
* [Report Issues Here](https://github.com/libretro/beetle-psx-libretro/issues)
