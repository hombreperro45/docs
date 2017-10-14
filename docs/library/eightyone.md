# ZX81 (EightyOne)

## Background

EightyOne is a port of the EightyOne (a.k.a. THE Sinclair Emulator) to libretro.

Author(s):

Michael D Wynne

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/eightyone.md). Changes are proposed using "Pull Requests."

## License

GPLv3

## Extensions

p|tzx|t81

## BIOS

The EightyOne core does not feature BIOS use.

## Features

| Feature           | Supported |
|-------------------|:---------:|
| Saves             | ✕         |
| States            | ✔         |
| Rewind            | ✔         |
| Netplay           | ✔         |
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

The EightyOne core creates directories named EightyOne in RetroArch's save and state directories 

Save states are saved/loaded to and from the core's state directory. 

## Options

The EightyOne core has the following options that can be tweaked from the core options menu. The default setting is bolded.

- **Tape Fast Load** (Off/**On**): Instantly loads files if enabled, or disabled it to see the moving horizontal lines while the game loads.
- **8K-16K Contents** (**auto**/ROM shadow/RAM/dK'tronics 4K Graphics ROM + 4K RAM): Selects the contents of memory addresses between 8192 and 16383, a shadow copy of the ROM, 8K of RAM, or [dK'tronics 4K ROM plus 4K of RAM](http://www.fruitcake.plus.com/Sinclair/ZX81/Chroma/ChromaInterface_Software_CharacterSetROM.htm).
- **High Resolution** (**auto**/none/WRX): Enables WRX high resolution.
- **Emulate Chroma 81** (**auto**/Off/On): Enable the [Chroma 81](http://www.fruitcake.plus.com/Sinclair/ZX81/Chroma/ChromaInterface.htm) interface.
- **Video Presets** (**clean**/tv/noisy): Change how the video is emulated (if Chroma 81 is enabled, the video is set to "clean" regardless of this option).
- **Sound emulation** (**auto**/none/Zon X-81): Enables sound emulation.
- **Joypad button (up, down, left, right, a, b, x, y, l, r, l2, r2) mapping** (**auto**/default/new line/shift/space/./0/1/2/3/4/5/6/7/8/9/a/b/c/d/e/f/g/h/i/j/k/l/m/n/o/p/q/r/s/t/u/v/w/x/y/z): Maps a joypad button to a keyboard key, defaults are the cursor keys for the directional pad and '0' to all the other buttons
- **Transparent Keyboard Overlay** (Off/**On**): If the keyboard overlay is transparent or opaque.
- **Time to Release Key in ms** (**100**/300/500/1000): How many milliseconds to wait before releasing the key pressed using the keyboard overlay.

## Controllers

The EightyOne core supports 3 controller setting(s), the bolded controller setting is default:

## Device Types available to all users

* **RetroPad** - [Joypad] - *Awaiting description.*

## User 1 exclusive Device Types

* Cursor Joystick - [Joypad] - *Awaiting description.*

## User 2 exclusive Device Types

* Sinclair Keyboard - [Keyboard] - *Switch to this to be able to use your keyboard*

| EightyOne | **RetroPad**                                                   | Cursor Joystick |
|-----------|----------------------------------------------------------------|-----------------|
|           | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               |                 |
|           | ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               |                 |
|           | ![RetroPad_Select](images/RetroPad/Retro_Select.png)           |                 |
|           | ![RetroPad_Start](images/RetroPad/Retro_Start.png)             |                 |
|           | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Up.png)            |                 |
|           | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Down.png)          |                 |
|           | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Left.png)          |                 |
|           | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Right.png)         |                 |
|           | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               |                 |
|           | ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               |                 |
|           | ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   |                 |
|           | ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   |                 |
|           | ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              |                 |
|           | ![RetroPad_R2](images/RetroPad/Retro_R2.png)                   |                 |
|           | ![RetroPad_L3](images/RetroPad/Retro_L3.png)                   |                 |
|           | ![RetroPad_R3](images/RetroPad/Retro_R3.png)                   |                 |
|           | ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)   |                 |
|           | ![RetroPad_Right_Stick](images/RetroPad/Retro_Right_Stick.png) |                 |

| RetroKeyboard| Sinclair Keyboard |
|--------------|-------------------|

## Compatibility

The EightyOne libretro core only emulates the Sinclair ZX81 with 16Kb RAM for now.

## External Links

* [Libretro Repository](https://github.com/libretro/81-libretro)
* [Report Core Issues Here](https://github.com/libretro/libretro-meta)
* [Official Repository](https://sourceforge.net/projects/eightyone-sinclair-emulator/)
