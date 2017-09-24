# PlayStation (Beetle PSX)

## Background

Beetle PSX is the Libretro fork of the Sony Playstation 1 emulator Mednafen PSX.

Author(s): Mednafen Team

## Contribute to this documentation

+In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/beetle_psx.md). Changes are proposed using "Pull Requests."

## See also

[Beetle PSX HW](https://buildbot.libretro.com/docs/library/beetle_psx_hw/)

## License

GPLv2

## Extensions

cue|toc|m3u|ccd|exe|pbp|chd

## BIOS

Beetle PSX requires the following BIOS image files for operation. **Case Sensitive**

|   Filename    |    Description                                         |              md5sum              |
|:-------------:|:------------------------------------------------------:|:--------------------------------:|
|  scph5500.bin |NTSC-J (Japan)                                          | 8dd7d5296a650fac7319bce665a6a53c |
|  scph5501.bin |NTSC-U/C (USA, Canada, Brazil and some of South America)| 490f666e1afb15b7362b406ed1cea246 |
|  scph5502.bin |PAL (UK, Spain, France, most of Europe and Australia)   | 32736f17079d0b2b7024407c39bd3050 |

## Features

| Saves | States      | Rewind | Netplay | RetroAchievements | RetroArch Cheats | Native Cheats |
|:-----:|:-----------:|:------:|:-------:|:-----------------:|:----------------:|:-------------:|
| Yes   |   Yes*      | Yes*   |   No    |        -          |   -              | -             |

| Controllers     | Multi-Mouse | Rumble | Sensors | Camera | Location | Subsystem     |
|:---------------:|:-----------:|:------:|:-------:|:------:|:--------:|:--------------|
|       No        |      -      |   Yes  |   No    |   No   |   No     |       No      |

## Usage

Beetle PSX can load CD-ROM games from a ripped/dumped copy of the disc, such as CUE+BIN. Additionally there is support for CloneCD "CCD/IMG/SUB" rips, cdrdao "TOC" files and compressed file types "PBP/CHD". You can also utilise a .M3U file for multi disc games.

## Loading content

Beetle PSX HW needs a cue-sheet that points to an image file. A cue sheet, or cue file, is a metadata file which describes how the tracks of a CD or DVD are laid out.

Example Cue Sheet for "Mega Man 8 (USA)"

`Mega Man 8 (USA).cue`
```
    FILE "Mega Man 8 (USA) (Track 1).bin" BINARY
        TRACK 01 MODE2/2352
            INDEX 01 00:00:00

    FILE "Mega Man 8 (USA) (Track 2).bin" BINARY
        TRACK 02 AUDIO
            INDEX 00 00:00:00
            INDEX 01 00:02:00

    FILE "Mega Man 8 (USA) (Track 3).bin" BINARY
        TRACK 03 AUDIO
            INDEX 00 00:00:00
            INDEX 01 00:02:00
```

Most PS1 games are single-track, so the cue file contents should look like this:

`foobin.cue`
```
 FILE "foo.bin" BINARY
  TRACK 01 MODE1/2352
   INDEX 01 00:00:00
```
## Multiple-disk games

If foo is a multiple-disk game, you should have .cue/.ccd/.toc files for each one, e.g. `foo (Disc 1).cue`, `foo (Disc 2).cue`, `foo (Disc 3).cue`.

To take advantage of Beetle PSX Disk Control feature for disk swapping, an index file (a m3u file) should be made.

Create a text file and save it as `foo.m3u`. Then enter your game's .cue files on it. The m3u file contents should look something like this:

`foo.m3u`
```
foo (Disc 1).cue
foo (Disc 2).cue
foo (Disc 3).cue
```

After that, you can load the `foo.m3u` file in RetroArch with the Beetle PSX core.

!!! note
    Adding multi-track games to playlists manually is recommended. (Add an entry in the playlist that points to `foo.m3u`)

An alternative is to append disks to the current playlist via RetroArch menu. A side advantage of the M3U method vs. the Append Disk method is that memory cards are named after the playlist itself, so you don't have different saves for different disks of the same game.

## Options

The (Beetle PSX) core has the following options that can be tweaked from the core options menu. The default setting is bolded.

- **CD image cache** (**Off**/On) (**Restart**): preloads the entire CD image into memory at startup. It causes a small delay at start-up but alleviates small hiccups that can be cause by emulated CD access, this setting is recommended unless you have a system with very low memory.
- **Widescreen mode hack** (**Off**/On): If on, renders in 16:9. Works best on 3D games.
- **Frame duping (speedup)** (**Off**/On): Redraws/reuses the last frame if there was no new data.
- **CPU Overclock** (**Off**/On): Gets rid of memory access latency and makes all GTE instructions have 1 cycle latency.
- **Skip BIOS** (**Off**/On): Self-explanatory. Some games have issues when enabled.
- **Dithering pattern** (**1x(native)**/internal resolution/Off): If off, disables the dithering pattern the PSX applies to combat color banding. OpenGL only. Vulkan always disables the pattern.
- **Display internal FPS** (**Off**/On): Shows the frame rate at which the emulated PSX is drawing at. Onscreen Notifications must be enabled in the RetroArch Onscreen Display Settings.
- **Initial scanline** (**0** - 40): Sets the first scanline to be drawn on screen.
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
