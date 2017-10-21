# SNES / Super Famicom (bsnes Accuracy)

## Background

bsnes is a Super Nintendo emulator that began development on 2004-10-14. It focuses on accuracy and clean code above all else. It never uses speed or compatibilty hacks. As a result, the minimum system requirements are greater than with other emulators. bsnes comes in three different profiles (accuracy, balanced and performance) which contain minor differences in the PPU (graphics) emulation. 

This core has been compiled with the Accuracy profile.

Author(s):

byuu

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/bsnes_accuracy.md). Changes are proposed using "Pull Requests."

## See also

[bsnes Balanced](https://buildbot.libretro.com/docs/library/bsnes_balanced/)

[bsnes Performance](https://buildbot.libretro.com/docs/library/bsnes_performance/)

[bsnes-mercury Accuracy](https://buildbot.libretro.com/docs/library/bsnes_mercury_accuracy/)

[bsnes-mercury Balanced](https://buildbot.libretro.com/docs/library/bsnes_mercury_balanced/)

[bsnes-Mercury Performance](https://buildbot.libretro.com/docs/library/bsnes_performance/)

[Beetle bsnes](https://buildbot.libretro.com/docs/library/beetle_snes/)

[bsnes C++98 (v085)](https://buildbot.libretro.com/docs/library/bsnes_cplusplus98/)

## License

GPLv3

## Extensions

sfc|smc|bml

## BIOS

Required or optional firmware files go in RetroArch's system directory.

The bsnes Accuracy core uses split ROMS for [special chip games](https://en.wikipedia.org/wiki/List_of_Super_NES_enhancement_chips#List_of_Super_NES_games_that_use_enhancement_chips).

Notable DSP1/DSP1B Games: Super Mario Kart, Pilotwings

Notable DSP2 Games: Dungeon Master

Notable DSP3 Games: SD Gundam GX

Notable DSP4 Games: Top Gear 3000

Notable Cx4 Games: Mega Man X2, Mega Man X3

|   Filename        |    Description              |              md5sum              |
|:-----------------:|:---------------------------:|:--------------------------------:|
| dsp1.data.rom     | DSP1 co-processor firmware  | 3d81b45fa0c2aa8b852dfb1ece7c0971 |
| dsp1.program.rom  | DSP1 co-processor firmware  | ae209fbe789fbf11a48aea5ab1197321 |
| dsp1b.data.rom    | DSP1B co-processor firmware | 1e3f568634a7d8284020dddc0ae905bc |
| dsp1b.program.rom | DSP1B co-processor firmware | d10f446888e097cbf500f3f663cf4f6d |
| dsp2.data.rom     | DSP2 co-processor firmware  | e9417e29223b139c3c4b635a2a3b8744 |
| dsp2.program.rom  | DSP2 co-processor firmware  | aa6e5922a3ed5ded54f24247c11143c5 |
| dsp3.data.rom     | DSP3 co-processor firmware  | 0a81210c0a940b997dd9843281008ee6 |
| dsp3.program.rom  | DSP3 co-processor firmware  | d99ca4562818d49cee1f242705bba6f8 |
| dsp4.data.rom     | DSP4 co-processor firmware  | ee4990879eb68e3cbca239c5bc20303d |
| dsp4.program.rom  | DSP4 co-processor firmware  | a151023b948b90ffc23a5b594bb6fef2 |
| cx4.data.rom      | CX4 co-processor firmware   | 037ac4296b6b6a5c47c440188d3c72e3 |
| st010.data.rom    | ST010 co-processor firmware | 254d70762b6f59f99c27c395aba7d07d |
| st010.program.rom | ST010 co-processor firmware | 1d70019179a59a566a0bb5d3f2845544 |
| st011.data.rom    | ST011 co-processor firmware | 10bd3f4aa949737ab9836512c35bcc29 |
| st011.program.rom | ST011 co-processor firmware | 95222ebf1c0c2990bcf25db43743f032 |
| st018.data.rom    | ST018 co-processor firmware | 49c898b60d0f15e90d0ba780dd12f366 |
| st018.program.rom | ST018 co-processor firmware | dda40ccd57390c96e49d30a041f9a9e7 |
| sgb.boot.rom      | SGB Boot Image              | d574d4f9c12f305074798f54c091a8b4 |

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
| Multi-Mouse       | -         |
| Rumble            | ✕         |
| Sensors           | ✕         |
| Camera            | ✕         |
| Location          | ✕         |
| Subsystem         | ✔         |

The bsnes Accuracy core creates directories named 'bsnes' in RetroArch's save and state directories

Game data is saved/loaded to and from the core's save directory.

Save states are saved/loaded to and from the core's state directory. 

## Options

The bsnes Accuracy core does not feature core options.

## Controllers

The bsnes Accuracy core supports 6 controller setting(s), the bolded controller setting is default:

The bsnes Accuracy core supports a max of 5 users.

### User 1 and 2 exclusive Device Types

* **[SNES Joypad](http://nintendo.wikia.com/wiki/Super_Nintendo_Entertainment_System_controller)** - [Joypad without analog]

* [SNES Mouse](https://en.wikipedia.org/wiki/Super_NES_Mouse) - [Mouse]

### User 2 exclusive Device Types

* [Multitap](http://nintendo.wikia.com/wiki/Super_Multitap) - [Joypad] - allows for up to five players to play together in certain games.

* [SuperScope](https://en.wikipedia.org/wiki/Super_Scope) - [Lightgun]

* [Justifier](https://en.wikipedia.org/wiki/Konami_Justifier) - [Lightgun]

* [Justifiers](https://en.wikipedia.org/wiki/Konami_Justifier) - [Lightgun]

| bsnes Accuracy | RetroPad                                               | SNES Joypad                                             |
|----------------|--------------------------------------------------------|---------------------------------------------------------|
| B              | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)       | ![SNES_B](images/Button_Pack/SNES/SNES_B.png)           |
| Y              | ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)       | ![SNES_Y](images/Button_Pack/SNES/SNES_Y.png)           |
| Select         | ![RetroPad_Select](images/RetroPad/Retro_Select.png)   | ![SNES_Select](images/Button_Pack/SNES/SNES_Select.png) |
| Start          | ![RetroPad_Start](images/RetroPad/Retro_Start.png)     | ![SNES_Start](images/Button_Pack/SNES/SNES_Start.png)   |
| D-Pad Up       | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Up.png)    | ![SNES_Dpad](images/Button_Pack/SNES/SNES_Dpad.png)     |
| D-Pad Down     | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Down.png)  | ![SNES_Dpad](images/Button_Pack/SNES/SNES_Dpad.png)     |
| D-Pad Left     | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Left.png)  | ![SNES_Dpad](images/Button_Pack/SNES/SNES_Dpad.png)     |
| D-Pad Right    | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Right.png) | ![SNES_Dpad](images/Button_Pack/SNES/SNES_Dpad.png)     |
| A              | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)       | ![SNES_A](images/Button_Pack/SNES/SNES_A.png)           |
| X              | ![RetroPad_X](images/RetroPad/Retro_X_Round.png)       | ![SNES_X](images/Button_Pack/SNES/SNES_X.png)           |
| L              | ![RetroPad_L1](images/RetroPad/Retro_L1.png)           | ![SNES_L](images/Button_Pack/SNES/SNES_L.png)           |
| R              | ![RetroPad_R1](images/RetroPad/Retro_R1.png)           | ![SNES_R](images/Button_Pack/SNES/SNES_R.png)           |

| RetroMouse                                                                                                      | SNES Mouse   | SuperScope | Justifier(s) |
|-----------------------------------------------------------------------------------------------------------------|--------------|------------|--------------|
| ![Retro_Mouse](images/RetroMouse/Retro_Mouse.png)                                                               | Pointer      | Pointer    | Pointer      |
| ![Retro_Left](images/RetroMouse/Retro_Left.png)                                                                 | Left Button  | Trigger    | Trigger      |
| ![Retro_Middle](images/RetroMouse/Retro_Middle.png)                                                             |              | ???        |              |
| ![Retro_Right](images/RetroMouse/Retro_Right.png)                                                               | Right Button | Turbo      | Turbo        |
| ![Retro_Left+Middle](images/RetroMouse/Retro_Left+Middle.png)                                                   |              | Pause      | Pause        |
| ![Retro_Right+Middle](images/RetroMouse/Retro_Right+Middle.png)                                                 |              | Start      | Start        |
| ![Retro_Left+Middle](images/RetroMouse/Retro_Left+Middle.png) + ![Retro_Left](images/RetroMouse/Retro_Left.png) |              | Reset      | Reset        |

## Compatibility

The bsnes Accuracy core fully emulates all SNES games that have ever been officially released. 

### Super Gameboy Support

Super Gameboy is supported via the Subsystem API. In RetroArch the Subsystem API is only available via [CLI](https://buildbot.libretro.com/docs/guides/cli-intro/).
For SGB support you need both sgb.boot.rom and the SGB rom.

#### To launch SGB games, launch RetroArch like this:
    retroarch -L {path to bsnes core} {path to snes rom} --subsystem sgb {path to gb rom}

## External Links

* [Libretro Repository](https://github.com/libretro/bsnes-libretro)
* [Report Core Issues Here](https://github.com/libretro/libretro-meta)
* [Official Website](https://byuu.org/)
* [Official Upstream Downloads](https://byuu.org/emulation/higan/)