# Atari ST/STE/TT/Falcon (Hatari)

## Background

Hatari is an Atari ST/STE/TT/Falcon system emulator that can be used as a libretro core. Hatari tries to emulate the hardware as close as possible so that it is able to run most of the old Atari games and demos.

Author(s): Nicolas Pomarède

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/blob/master/docs/library/hatari.md). Changes are proposed using "Pull Requests."

## License

GPLv2

## Extensions

st|msa|zip|stx|dim|ipf

## BIOS

|   Filename    |    Description        |              md5sum              |
|:-------------:|:---------------------:|:--------------------------------:|
|tos.img        |          TOS Boot Image - Required            | c1c57ce48e8ee4135885cee9e63a68a2 |

## Features

| Saves | States      | Rewind | Netplay | RetroAchievements | RetroArch Cheats | Native Cheats |
|:-----:|:-----------:|:------:|:-------:|:-----------------:|:----------------:|:-------------:|
|  -    |     no      |   no   |   no    |        no         |   no             | -             |

| Controllers     | Rumble | Sensors | Camera | Location | Subsystem     |
|:---------------:|:------:|:-------:|:------:|:--------:|:-------------:|
|        no       |   no   |    no   |   no   |    no    |       no      |

## Options

The Hatari core has the following options that can be tweaked from the core options menu. The default setting is bolded. 

- **Internal resolution** (**640x480**/832x576/832x588/800x600/960x720/1024x768/1024x1024): Sets internal resolution

## Controllers

The Hatari core supports one controller setting(s):

* RetroPad

[hatari_retropad](images/Controllers/hatari_retropad.png)

| Hatari             | [RetroPad](RetroPad)                                           |
|--------------------|----------------------------------------------------------------|
|                    | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               |
| Enter GUI          | ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               |
| Mouse mode toggle  | ![RetroPad_Select](images/RetroPad/Retro_Select.png)           |
| Keyboard overlay   | ![RetroPad_Start](images/RetroPad/Retro_Start.png)             |
| D-pad              | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)               |
| Fire               | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               |
|                    | ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               |
| Joystick number    | ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   |
| Mouse speed        | ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   |
| Toggle m/k status  | ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              |
|                    | ![RetroPad_R2](images/RetroPad/Retro_R2.png)                   |
|                    | ![RetroPad_L3](images/RetroPad/Retro_L3.png)                   |
|                    | ![RetroPad_R3](images/RetroPad/Retro_R3.png)                   |
|                    | ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)   |
|                    | ![RetroPad_Right_Stick](images/RetroPad/Retro_Right_Stick.png) |

## Compatibility

Hatari compatibility can be found [here](https://hg.tuxfamily.org/mercurialroot/hatari/hatari/raw-file/tip/doc/compatibility.html)

## External Links

* [Libretro Repository](https://github.com/libretro/hatari)
* [Report Libretro Issues Here](https://github.com/libretro/libretro-meta/issues)
* [Official Website](http://hatari.tuxfamily.org/)
* [Official Upstream Downloads](http://hatari.tuxfamily.org/download.html)
