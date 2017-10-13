# Title

(Check the display name entry in the relevant core info file (https://github.com/libretro/libretro-super/tree/master/dist/info))

## Background

Author(s):

(Use internet aliases whenever possible)

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/). Changes are proposed using "Pull Requests."

(add relevent corenamed.md to end of link) 

(There's already an edit button on all the documentation pages but having another contribution link doesn't hurt.)

## See also

[Other Core](https://buildbot.libretro.com/docs/library/)

(OPTIONAL SECTION, add related cores url endings to end of link)

## License

(Check the license entry in the relevant core info file (https://github.com/libretro/libretro-super/tree/master/dist/info) or check the core's repository for license information)

## Extensions

--If no extensions use--
The (Core name) core does not feature extension use.

(Check the supported extensions entry in the relevant core info file (https://github.com/libretro/libretro-super/tree/master/dist/info))
(Extensions such as cue or m3u will eventually have a hyperlink for their respective guides)

## BIOS

Required or optional firmware files go in RetroArch's system directory.

|   Filename    |    Description         |              md5sum              |
|:-------------:|:----------------------:|:--------------------------------:|
| optional.bin  | Description - Optional |                                  |
| required.bin  | Description - Required |                                  |

(Check the firmware information in the relevant core info file (https://github.com/libretro/libretro-super/tree/master/dist/info))

--If no BIOS use--
The (Core name) core does not feature BIOS use.

## Features

| Feature           | Supported |
|-------------------|:---------:|
| Saves             | ✔         |
| States            | ✕         |
| Rewind            | ✕         |
| Netplay           | ✕         |
| RetroAchievements | ✕         |
| RetroArch Cheats  | ✕         |
| Native Cheats     | ✕         |
| Controllers       | ✕         |
| Multi-Mouse       | ✕         |
| Rumble            | ✕         |
| Sensors           | ✕         |
| Camera            | ✕         |
| Location          | ✕         |
| Subsystem         | ✕         |

(State support can be tested by attempting to save and load a state in the core)
(If States are supported, that means Rewind and Netplay are supported too)

The (Core name) creates directories named (Folder name) in RetroArch's save and state directories 

(Describe what the core reads/writes to and from the save and state directories)

## Options

The (Core name) core has the following options that can be tweaked from the core options menu. The default setting is bolded.

- **Core Option** (**Setting1**/Setting2): Description.
- **Core Option 2** (**Setting1**/Setting2): Description.

--If no options use--
The (Core name) core does not feature core options.

## Controllers

The (Core name) core supports # controller setting(s), the bolded controller setting is default:

* **RetroPad** - [Joypad]

| Core Name | RetroPad                                                       |
|-----------|----------------------------------------------------------------|
| Action 1  | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               |
| Action 2  | ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)               |
| Action 3  | ![RetroPad_Select](images/RetroPad/Retro_Select.png)           |
| Action 4  | ![RetroPad_Start](images/RetroPad/Retro_Start.png)             |
| Action 5  | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Up.png)            |
| Action 5  | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Down.png)          |
| Action 5  | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Left.png)          |
| Action 5  | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Right.png)         |
| Action 6  | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               |
| Action 7  | ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               |
| Action 8  | ![RetroPad_L1](images/RetroPad/Retro_L1.png)                   |
| Action 9  | ![RetroPad_R1](images/RetroPad/Retro_R1.png)                   |
| Action 10 | ![RetroPad_L2](images/RetroPad/Retro_L2_Temp.png)              |
| Action 11 | ![RetroPad_R2](images/RetroPad/Retro_R2.png)                   |
| Action 12 | ![RetroPad_L3](images/RetroPad/Retro_L3.png)                   |
| Action 13 | ![RetroPad_R3](images/RetroPad/Retro_R3.png)                   |
| Action 14 | ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)   |
| Action 15 | ![RetroPad_Right_Stick](images/RetroPad/Retro_Right_Stick.png) |

| RetroMouse                                                      |
|-----------------------------------------------------------------|
| ![Retro_Mouse](images/RetroMouse/Retro_Mouse.png)               | 
| ![RetroP_Left](images/RetroMouse/Retro_Left.png)                |
| ![Retro_Middle](images/RetroMouse/Retro_Middle.png)             | 
| ![Retro_Right](images/RetroMouse/Retro_Right.png)               | 
| ![Retro_Left+Middle](images/RetroMouse/Retro_Left+Middle.png)   | 
| ![Retro_Right+Middle](images/RetroMouse/Retro_Right+Middle.png) |

(Controllers is a potentially complex section (e.g. Genesis Plus GX core doc), filling out this section may require looking at the core's source code (e.g. libretro.c) to find what the buttons are bound to.) 

(RETROMOUSE TABLE IS OPTIONAL, the table is for cores that have mouse driven device types)

## Compatibility

--Use [(Core name) Core Compatibility List](URL) or make a table--

--If no compatibility issues--
The (Core name) core does not have specific compatiblity issues

--If no concrete compatiblity information can be found--
Unknown

## External Links

--Standard links but doesn't need to exactly match this--
* [Libretro Repository](https://link)
* [Report Core Issues Here](https://github.com/libretro/libretro-meta)
* [Official Website](https://link)
* [Official Repository](https://link)
