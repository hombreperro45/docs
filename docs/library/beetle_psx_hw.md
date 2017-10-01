# PlayStation (Beetle PSX HW)

## Background

Enhanced port of standalone Mednafen PSX to libretro.

Author(s): Mednafen Team

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/blob/master/docs/library/beetle_psx_hw.md). Changes are proposed using "Pull Requests."

## License

GPLv2

## Extensions

cue|toc|m3u|ccd|exe|pbp|chd

## BIOS

|   Filename  | Description |              md5sum             |
|:-----------:|:-----------:|:-------------------------------:|
|scph5500.bin |PS1 JP BIOS - Required for JP  |8dd7d5296a650fac7319bce665a6a53c |
|scph5501.bin |PS1 US BIOS - Required for US  |490f666e1afb15b7362b406ed1cea246 |
|scph5502.bin |PS1 EU BIOS - Required for EU  |32736f17079d0b2b7024407c39bd3050 |

## Features

| Saves | States      | Rewind | Netplay | RetroAchievements | RetroArch Cheats | Native Cheats |
|:-----:|:-----------:|:------:|:-------:|:-----------------:|:----------------:|:-------------:|
|  yes  |   yes       | yes    | yes     |       no          | yes              | no            |

| Controllers     | Rumble | Sensors | Camera | Location | Subsystem     |
|:---------------:|:------:|:-------:|:------:|:--------:|:-------------:|
|      yes        | yes    |   no    |  no    |   no     |      no       |

## Running

To run this core, The appropriate PSX BIOS must be placed in RetroArch's system directory.

## Loading content

Beetle PSX HW needs a cue-sheet that points to an image file. A cue sheet, or cue file, is a metadata file which describes how the tracks of a CD or DVD are laid out.

If you have e.g. `foo.bin`, you should create a text file and save it as `foo.cue`. Most PS1 games are single-track, so the cue file contents should look like this:

`foobin.cue`
```
 FILE "foo.bin" BINARY
  TRACK 01 MODE1/2352
   INDEX 01 00:00:00
```

After that, you can load the `foo.cue` file in RetroArch with the Beetle PSX HW core.

!!! warning
    Certain PS1 games are multi-track, so their .cue files might be more complicated.

## Multiple-disk games

If foo is a multiple-disk game, you should have .cue files for each one, e.g. `foo (Disc 1).cue`, `foo (Disc 2).cue`, `foo (Disc 3).cue`.

To take advantage of Beetle PSW HW's Disk Control feature for disk swapping, an index file (a m3u file) should be made.

Create a text file and save it as `foo.m3u`. Then enter your game's .cue files on it. The m3u file contents should look something like this:

`foo.m3u`
```
foo (Disc 1).cue
foo (Disc 2).cue
foo (Disc 3).cue
```

After that, you can load the `foo.m3u` file in RetroArch with the Beetle PSX HW core.

Adding multi-track games to playlists manually is recommended. (Add an entry in the playlist that points to `foo.m3u`)

## Game compression

Alternatively to using cue sheets with .bin files, you can convert your games to .pbp (Playstation Portable update file) to reduce file sizes and neaten up your game folder. A recommended .pbp convert tool is PSX2PSP.

If converting a multiple-disk game, all disks should be added to the same .pbp file, rather than making a .m3u file for them.

Most conversion tools will want a single .bin file for each disk. If your game uses multiple .bin files (tracks) per disk, you will have to mount the cue sheet to a virtual drive and re-burn the images onto a single track before conversion.

!!! note
    RetroArch does not currently have .pbp database due to variability in users' conversion methods. All .pbp games will have to be added to playlists manually.

## Saves

Memcard slot 0 is saved using libretro's standard interface (`gamename.srm`). You might have to rename your old memory cards brought from other emulators to `gamename.srm`.

The rest of memory cards are saved using Mednafen's standard mechanism. (e.g. `gamename.1.mcr`).

The game name in the Memcard filename will match the cue or m3u or pbp file's name, like this:

* Loaded content: `Breath of Fire III (USA).cue`

* Memcard slot 0: `Breath of Fire III (USA).srm`

* Memcard slot 1: `Breath of Fire III (USA).1.mcr`

or

* Loaded content: `Final Fantasy VII (USA).m3u`

* Memcard slot 0: `Final Fantasy VII (USA).srm`

* Memcard slot 1: `Final Fantasy VII (USA).1.mcr`

or

* Loaded content: `Wild Arms 2 (USA).pbp`

* Memcard slot 0: `Wild Arms 2 (USA).srm`

* Memcard slot 1: `Wild Arms 2 (USA).1.mcr`

!!! note
    Memory card behavior can be altered with any of the following core options (Memcard 0 method, Enable memory card 1, Shared memcards).

## Options

The Beetle PSW HW core has the following options that can be tweaked from the core options menu. The default setting is bolded. 

- **Renderer (restart)** (software/**vulkan**/opengl): The software renderer is the most accurate renderer. The opengl and vulkan options will enable and/or speedup enhancements like upscaling and texture filtering. The OpenGL and Vulkan renderers must be used with it's corresponding video driver, RetroArch's video driver can be changed in the RetroArch Driver settings. Also, Hardware Shared Context must be enabled in RetroArch's Core settings.
- **Software framebuffer** (Off/**On**): If off, the software renderer will skip some steps. Potential speedup. Causes bad graphics when doing framebuffer readbacks.
- **Adaptive smoothing** (Off/**On**): When upscaling, smooths out 2D elements while keeping 3D elements sharp. Vulkan renderer only at the moment.

??? note "*Adapative smoothing - Off*"
    ![adaptive_smoothing_off]((images\Cores\beetle_psx_hw\adaptive_smoothing_off.png)

??? note "*Adaptive smoothing - On*"
    ![adaptive_smoothing_on]((images\Cores\beetle_psx_hw\adaptive_smoothing_on.png)

- **Internal GPU Resolution** (**1x(native)**/2x/4x/8x/16x/32x): Graphics upscaling.

??? note "*Internal GPU Resolution - 1x*"
    ![internal_gpu_resolution_1](images\Cores\beetle_psx_hw\internal_gpu_resolution_1.png)

??? note "*Internal GPU Resolution - 2x*"
    ![internal_gpu_resolution_2](images\Cores\beetle_psx_hw\internal_gpu_resolution_2.png)

- **Texture filtering** (**nearest**/SABR/xBR/bilinear/3-point/JINC2): Per-texture filtering. OpenGL only at the moment. 

??? note "*nearest*"
    ![nearest](images\Cores\beetle_psx_hw\nearest.png)

??? note "*SABR*"
    ![nearest](images\Cores\beetle_psx_hw\SABR.png)

??? note "*xBR*"
    ![nearest](images\Cores\beetle_psx_hw\xBR.png)

??? note "*bilinear*"
    ![nearest](images\Cores\beetle_psx_hw\bilinear.png)

??? note "*3-point*"
    ![nearest](images\Cores\beetle_psx_hw\3-point.png)

??? note "*JINC2*"
    ![nearest](images\Cores\beetle_psx_hw\JINC2.png)

- **Internal color depth** (**dithered 16bpp (native)**/32bpp): PSX had 16bpp depth, beetle-psx can go up to 32bpp. OpenGL only at the moment. Vulkan always uses 32bpp.
- **Wireframe mode** (**Off**/On ): Shows only the outlines of polygons. OpenGL only. For debug use.
- **Display full VRAM** (**Off**/On): Everything in VRAM is drawn on screen. For debug use.
- **PGXP operation mode** (**Off**/memory only/memory + cpu ): When not off, floating point coordinates will be used for vertex positions, to avoid the PSX polygon jitter. 'memory + cpu' mode can further reduce jitter at the cost of performance and geometry glitches.
- **PGXP vertex cache** (**Off**/On): Maintains a cache for vertices. May result in better performance but can result in graphics glitches in most games.
- **PGXP perspective correct texturing** (**Off**/On): Original PSX did affine texture mapping, resulting in e.g. crooked lines across walls. This fixes it.
- **Widescreen mode hack** (**Off**/On): If on, renders in 16:9. Works best on 3D games. 
- **Frame duping (speedup)** (**Off**/On): Redraws/reuses the last frame if there was no new data.
- **CPU Overclock** (**Off**/On): Gets rid of memory access latency and makes all GTE instructions have 1 cycle latency.
- **Skip BIOS** (**Off**/On): Self-explanatory. Some games have issues when enabled.
- **Dithering pattern** (**1x(native)**/internal resolution/Off): If off, disables the dithering pattern the PSX applies to combat color banding. OpenGL only. Vulkan always disables the pattern.
- **Display internal FPS** (**Off**/On): Shows the frame rate at which the emulated PSX is drawing at. Onscreen Notifications must be enabled in the RetroArch Onscreen Display Settings.- **Initial scanline** (**0** - 40): Sets the first scanline to be drawn on screen.
- **Last scanline** (210 - **239**): Sets the last scanline to be drawn on screen.
- **Initial scanline PAL** (**0** - 40): Sets the first scanline to be drawn on screen for PAL systems.
- **Last scanline PAL** (260 - **287**): Sets the last scanline to be drawn on screen for PAL systems.
- **Crop Overscan** (Off/**On**):  Self-explanatory.
- **Additional Cropping** (**Off**/1 px - 8 px): Self-explanatory.
- **Offset Cropped Image** (**Off**/ -4 px - 4 px): Self-explanatory.
- **Analog self-calibration** (**Off**/On): Monitors the max values reached by the input, using it as a calibration heuristic which then scales the analog coordinates sent to the emulator accordingly. For best results, rotate the sticks at max amplitude for the algorithm to get a good estimate of the scaling factor, otherwise it will adjust while playing.
- **DualShock Analog button toggle** (**Off**/On): Toggles the Analog button from DualShock controllers, if disabled analogs are always on, if enabled you can toggle their state by pressing and holding START+SELECT+L1+L2+R1+R2.
- **Port 1: Multitap enable** (**Off**/On): Enables/Disables multitap functionality on port 1.
- **Port 2: Multitap enable** (**Off**/On): Enables/Disables multitap functionality on port 2.
- **CD Image Cache (restart)** (**Off**/On): Loads the complete image in memory at startup.
- **Memcard 0 method** (**libretro**/mednafen): Picks the format (libretro or mednafen) used for storing memcard 0 save data.
- **Enable memory card 1** (Off/**On**): Specifically enables memcard slot 1. Needed for game "Codename Tenka".
- **Shared memcards (restart)** (**Off**/On): Stores everything in the same savefile. 'Memcard 0 method' needs to be set to 'libretro'. 

## Controllers

The Beetle PSW HW core supports four controller(s):

* PS1 Joypad

![beetle_psx_hw_ps1joypad](images/Controllers/beetle_psx_hw_ps1joypad.png)

* DualAnalog

![beetle_psx_hw_dualanalog](images/Controllers/beetle_psx_hw_dualanalog)

* DualShock

![beetle_psx_hw_dualshock](images/Controllers/beetle_psx_hw_dualshock)

* FlightStick

![beetle_psx_hw_flightstick](images/Controllers/beetle_psx_hw_flightstick)

For normal analog stick usage with the DualAnalog and DualShock device type, make sure the corresponding user's Analog to Digital Type is set to none.

Rumble only works when the corresponding user's device type is set to DualShock and the joypad input driver being used has rumble function implementation (e.g. Xinput).

| Beetle PSX HW                                                  | PS1 Joypad                                                     | DualAnalog                                                     | DualShock                                                      | FlightStick                                                    |
|----------------------------------------------------------------|----------------------------------------------------------------|----------------------------------------------------------------|----------------------------------------------------------------|----------------------------------------------------------------|
| ![PS3_Cross](images/Button_Pack/PS3/PS3_Cross.png)             | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               |
| ![PS3_Square](images/Button_Pack/PS3/PS3_Square.png)           | ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               | ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               | ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               | ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               |
| ![PS3_Select](images/Button_Pack/PS3/PS3_Select.png)           | ![RetroPad_Select](images/RetroPad/Retro_Select.png)           | ![RetroPad_Select](images/RetroPad/Retro_Select.png)           | ![RetroPad_Select](images/RetroPad/Retro_Select.png)           | ![RetroPad_Select](images/RetroPad/Retro_Select.png)           |
| ![PS3_Start](images/Button_Pack/PS3/PS3_Start.png)             | ![RetroPad_Start](images/RetroPad/Retro_Start.png)             | ![RetroPad_Start](images/RetroPad/Retro_Start.png)             | ![RetroPad_Start](images/RetroPad/Retro_Start.png)             | ![RetroPad_Start](images/RetroPad/Retro_Start.png)             |
| ![PS3_Dpad](images/Button_Pack/PS3/PS3_Dpad.png)               | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)               | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)               | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)               | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)               |
| ![PS3_Circle](images/Button_Pack/PS3/PS3_Circle.png)           | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               |
| ![PS3_Triangle](images/Button_Pack/PS3/PS3_Triangle.png)       | ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               | ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               | ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               | ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               |
| ![PS3_L1](images/Button_Pack/PS3/PS3_L1.png)                   | ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   | ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   | ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   | ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   |
| ![PS3_R1](images/Button_Pack/PS3/PS3_R1.png)                   | ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   | ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   | ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   | ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   |
| ![PS3_L2](images/Button_Pack/PS3/PS3_L2.png)                   | ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              | ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              | ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              | ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              |
| ![PS3_R2](images/Button_Pack/PS3/PS3_R2.png)                   | ![RetroPad_R2](images/RetroPad/Retro_R2.png)                   | ![RetroPad_R2](images/RetroPad/Retro_R2.png)                   | ![RetroPad_R2](images/RetroPad/Retro_R2.png)                   | ![RetroPad_R2](images/RetroPad/Retro_R2.png)                   |
| ![PS3_L3](images/Button_Pack/PS3/PS3_L3.png)                   |                                                                |                                                                | ![RetroPad_L3](images/RetroPad/Retro_L3.png)                   |                                                                |
| ![PS3_R3](images/Button_Pack/PS3/PS3_R3.png)                   |                                                                |                                                                | ![RetroPad_R3](images/RetroPad/Retro_R3.png)                   |                                                                |
| ![PS3_Left_Stick](images/Button_Pack/PS3/PS3_Left_Stick.png)   |                                                                | ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)   | ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)   | ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)   |
| ![PS3_Right_Stick](images/Button_Pack/PS3/PS3_Right_Stick.png) |                                                                | ![RetroPad_Right_Stick](images/RetroPad/Retro_Right_Stick.png) | ![RetroPad_Right_Stick](images/RetroPad/Retro_Right_Stick.png) | ![RetroPad_Right_Stick](images/RetroPad/Retro_Right_Stick.png) |

## Compatibility

Please file bugs that are reproducible on upstream standalone on the [official forums](https://forum.fobby.net/index.php?t=msg&th=1114&start=0&).

## External Links

* [Libretro Repository](https://github.com/libretro/beetle-psx-libretro)
* [Report Core Issues Here](https://github.com/libretro/libretro-meta/issues)
* [Official Website](https://mednafen.github.io/)
* [Official Upstream Downloads](https://mednafen.github.io/releases/)
