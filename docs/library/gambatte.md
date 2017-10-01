# Game Boy / Game Boy Color (Gambatte)

## Background

Gambatte is an accuracy-focused, open-source, cross-platform Game Boy Color emulator written in C++. It is based on hundreds of corner case hardware tests, as well as previous documentation and reverse engineering efforts.

Author(s): Sinamas

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/gambatte.md). Changes are proposed using "Pull Requests."

## License

GPLv2

## Extensions

gb|gbc|dmg

## BIOS

|   Filename    |    Description                 |              md5sum              |
|:-------------:|:------------------------------:|:--------------------------------:|
| gb_bios.bin   | Game Boy BIOS - Optional       | 32fbbd84168d3482956eb3c5051637f5 |
| gbc_bios.bin   | Game Boy Color BIOS - Optional | dbfce9db9deaa2567f6a84fde55f9680 |

## Features

| Saves | States      | Rewind | Netplay | RetroAchievements | RetroArch Cheats | Native Cheats |
|:-----:|:-----------:|:------:|:-------:|:-----------------:|:----------------:|:-------------:|
|  yes  |     yes     |   yes  |   no    |      yes          | yes              | no            |

| Controllers     | Rumble | Sensors | Camera | Location | Subsystem     |
|:---------------:|:------:|:-------:|:------:|:--------:|:-------------:|
|       no        |  no    |   no    |  no    |   no     |      no       |

## Options

The Gambatte core has the following options that can be tweaked from the core options menu. The default setting is bolded:

- **GB Colorization** (**Off**/auto/internal/custom): Colorizes Game Boy games.

??? note "*GB Colorization - Off*"
    ![gb_colorization_off](images\Cores\gambatte\gb_colorization_off.png)

??? note "*GB Colorization - auto*"
    ![gb_colorization_auto](images\Cores\gambatte\gb_colorization_auto.png)

- **Internal Palette** (**GBC - Blue**/GBC - Brown/GBC - Dark Blue/GBC - Dark Brown/GBC - Dark Green/GBC - Grayscale/GBC - Green/GBC - Inverted/GBC - Orange/GBC - Pastel Mix/GBC - Red/GBC - Yellow/Special 1/Special 2/Special 3): Select which internal color palette for GB Colorization is going to be used. GB Colorization must be set to internal.

??? note "*Internal Palette - GBC - Blue*"
    ![internal_palette_gbc_blue](images\Cores\gambatte\internal_palette_gbc_blue.png)

??? note "*Internal Palette - GBC - Brown*"
    ![internal_palette_gbc_brown](images\Cores\gambatte\internal_palette_gbc_brown.png)

??? note "*Internal Palette - GBC - Dark Blue*"
    ![internal_palette_gbc_dark_blue](images\Cores\gambatte\internal_palette_gbc_dark_blue.png)

??? note "*Internal Palette - GBC - Dark Brown*"
    ![internal_palette_gbc_dark_brown](images\Cores\gambatte\internal_palette_gbc_dark_brown.png)

??? note "*Internal Palette - GBC - Dark Green*"
    ![internal_palette_gbc_dark_green](images\Cores\gambatte\internal_palette_gbc_dark_green.png)

??? note "*Internal Palette - GBC - Grayscale*"
    ![internal_palette_gbc_grayscale](images\Cores\gambatte\internal_palette_gbc_grayscale.png)

??? note "*Internal Palette - GBC - Green*"
    ![internal_palette_gbc_green](images\Cores\gambatte\internal_palette_gbc_green.png)

??? note "*Internal Palette - GBC - Inverted*"
    ![internal_palette_gbc_inverted](images\Cores\gambatte\internal_palette_gbc_inverted.png)

??? note "*Internal Palette - GBC - Orange*"
    ![internal_palette_gbc_orange](images\Cores\gambatte\internal_palette_gbc_orange.png)

??? note "*Internal Palette - GBC - Pastel Mix*"
    ![internal_palette_gbc_pastel_mix](images\Cores\gambatte\internal_palette_gbc_pastel_mix.png)

??? note "*Internal Palette - GBC - Red*"
    ![internal_palette_gbc_red](images\Cores\gambatte\internal_palette_gbc_red.png)

??? note "*Internal Palette - GBC - Yellow*"
    ![internal_palette_gbc_yellow](images\Cores\gambatte\internal_palette_gbc_yellow.png)

??? note "*Internal Palette - GBC - Special 1*"
    ![internal_palette_gbc_special_1](images\Cores\gambatte\internal_palette_gbc_special_1.png)

??? note "*Internal Palette - GBC - Special 2*"
    ![internal_palette_gbc_special_2](images\Cores\gambatte\internal_palette_gbc_special_2.png)

??? note "*Internal Palette - GBC - Special 3*"
    ![internal_palette_gbc_special_3](images\Cores\gambatte\internal_palette_gbc_special_3.png)

- **Color Correction** (**On**/Off): Darkens Game Boy Color games to match the original hardware output.

??? note "*Color Correction - On*"
    ![color_correction_on](images\Cores\gambatte\color_correction_on.png)

??? note "*Color Correction - Off*"
    ![color_correction_off](images\Cores\gambatte\color_correction_off.png)

- **Emulated Hardware (restart)** (**Auto**/GB/GBC/GBA): Choose which hardware is emulated Game Boy, Game Boy Color, or Game Boy Advance
- **Use official bootloader (restart) (if available)** (**On**/Off): Enables support for using official Game Boy and Game Boy Color bootloaders with startup logos. Check BIOS section to see what files are needed.

??? note "*Game Boy bootloader*"
    ![use_official_bootloader_on_gb](images\Cores\gambatte\use_official_bootloader_on_gb.png)

??? note "*Game Boy Color bootloader*"
    ![use_official_bootloader_on_gbc](images\Cores\gambatte\use_official_bootloader_on_gbc.png)

- **Gameboy Link Mode:** (**Not Connected**/Network Server/Network Client)
- **Network Link Port:** (**56400**-56420)
- **Network link server add:** (**0**-255)
- **Network link server add:** (**0**-255)
- **Network link server add:** (**0**-255)
- **Network link server add:** (**0**-255)

## Custom palettes for Game Boy games

The GB Colorization core option must be set to custom.

Create a folder called "palettes" in RetroArch's system directory. Then, you can place custom palette files (.pal) inside the "palettes" folder

You can define different palettes for specific games by creating a .pal file in the "palettes" folder with "INTERNALROMNAME.pal" or "rom-name.pal". If no specific palette is found for a ROM then the default palette is used.

You can also define a palette to be used for all Game Boy games by creating a .pal file in the "palettes" folder named "Default.pal"

??? note "*Custom palettes can be created from the GUI in standalone Gambatte*"
    ![gambatte_standalone_palette_tool](images\Cores\gambatte\gambatte_standalone_palette_tool.png)

## Controllers

The Gambatte core supports one controller setting(s):

* RetroPad

![gambatte_retropad](images/Controllers/gambatte_retropad.png)

| Gambatte  | [RetroPad](RetroPad)                                           |
|-----------|----------------------------------------------------------------|
| B         | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               |
|           | ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               |
| Select    | ![RetroPad_Select](images/RetroPad/Retro_Select.png)           |
| Start     | ![RetroPad_Start](images/RetroPad/Retro_Start.png)             |
| D-pad     | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)               |
| A         | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               |
|           | ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               |
|           | ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   |
|           | ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   |
|           | ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              |
|           | ![RetroPad_R2](images/RetroPad/Retro_R2.png)                   |
|           | ![RetroPad_L3](images/RetroPad/Retro_L3.png)                   |
|           | ![RetroPad_R3](images/RetroPad/Retro_R3.png)                   |
|           | ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)   |
|           | ![RetroPad_Right_Stick](images/RetroPad/Retro_Right_Stick.png) |

## Compatibility

| Game                                  | Issue                          |
|---------------------------------------|--------------------------------|
|**Command Master**                     |Crashes on start. Unemulated MBC7 mapper. |
|**Game Boy Camera**|Crashes on start. Unemulated Pocket Camera mapper. |
|**Game de Hakken!! Tamagotchi - Osutchi to Mesutchi** |Crashes on start. Unemulated TAMA5 mapper. |
|**Kirby Tilt 'n' Tumble** |Crashes on start. Unemulated MBC7 mapper. |
|**Net de Get: Mini-Game @ 100**| 	Crashes on start. Unemulated MBC6 mapper. |
|**Pocket Family GB2**|Crashes on start. Unemulated HuC3 mapper. |
|**Robopon: Sun/Star/Moon Version**|Crashes on start. Unemulated HuC3 mapper. |

## External Links

* [Libretro Repository](https://github.com/libretro/gambatte-libretro)
* [Report Core Issues Here](https://github.com/libretro/libretro-meta)
* [Official Repository](https://github.com/sinamas/gambatte)
* [Old Standalone build downloads](https://sourceforge.net/projects/gambatte/files/gambatte/)
