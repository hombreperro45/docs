# Title

--Check the display name entry in the relevant core info file (https://github.com/libretro/libretro-super/tree/master/dist/info)--

## Background

--Use Google, Wikipedia, Github repository README's and descriptions for information--

### Author(s):

--Check the authors entry in the relevant core info file (https://github.com/libretro/libretro-super/tree/master/dist/info)--
--Use internet aliases whenever possible--

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/). Changes are proposed using "Pull Requests."

--add relevent corenamed.md to end of link-- 

## See also

[Other Core](https://buildbot.libretro.com/docs/library/)

--OPTIONAL SECTION, add all related cores url endings to end of link--

## License

--Check the license entry in the relevant core info file (https://github.com/libretro/libretro-super/tree/master/dist/info) or check the core's repository for license information--

## Extensions

Content that can be loaded by the (Core name) core.

--Check the supported extensions entry in the relevant core info file (https://github.com/libretro/libretro-super/tree/master/dist/info)--
--Extensions such as cue or m3u will eventually have a hyperlink for their respective guides--

--If no extensions use--
The (Core name) core does not feature extension use.

## Database(s)

RetroArch databases that are associated with the (Core name) core

--Check the database entry in the relevant core info file (https://github.com/libretro/libretro-super/tree/master/dist/info)--

## BIOS

Required or optional firmware files go in RetroArch's system directory.

|   Filename    |    Description         |              md5sum              |
|:-------------:|:----------------------:|:--------------------------------:|
| optional.bin  | Description - Optional |                                  |
| required.bin  | Description - Required |                                  |

--Check the firmware information in the relevant core info file (https://github.com/libretro/libretro-super/tree/master/dist/info)--

--If no BIOS use--
The (Core name) core does not feature BIOS use.

## Features

-- Use ✔ or ✕ or - --

| Feature           | Supported |
|-------------------|:---------:|
| Saves             | ✕         |
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

--State support can be tested by attempting to save and load a state in the core--
--If States are supported, that means Rewind and Netplay are supported too--

The (Core name) core creates directories named '(Folder name)' in RetroArch's save and state directories

--Describe what the core reads/writes to and from the save and state directories--

## Options

The (Core name) core has the following options that can be tweaked from the core options menu. The default setting is bolded.

- **Core Option** (**Setting1**/Setting2): Description.
- **Core Option 2** (**Setting1**/Setting2): Description.

--If no option use--
The (Core name) core does not feature core options.

## Controllers

--Controllers can be a potentially complex section (e.g. Genesis Plus GX core doc). Unforunately RetroArch's control menu may not have every input so filling out this section may require looking at the core's source code or libretro API documentation (e.g. libretro.cpp, libretro.c and libretro.h) to find what the buttons are bound to.--
--The first columns of the controller graph can be ripped straight from RetroArch's control menu--

The (Core name) core supports # controller setting(s), the bolded controller setting is default:

The (Core name) supports a max of # users.

### User # exclusive device types

* **RetroPad** - [Joypad without analog or Joypad with Analog or Keyboard or Mouse or Lightgun or Pointer] - Optional Description

| Core Name Input Descriptors | RetroPad                                                       |
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

| RetroKeyboard|
|--------------|

--RetroKeyboard table is optinal, the table is for cores that have keyboard driven device types--

| RetroMouse                                                      |
|-----------------------------------------------------------------|
| ![Retro_Mouse](images/RetroMouse/Retro_Mouse.png)               | 
| ![Retro_Left](images/RetroMouse/Retro_Left.png)                 |
| ![Retro_Middle](images/RetroMouse/Retro_Middle.png)             | 
| ![Retro_Right](images/RetroMouse/Retro_Right.png)               | 
| ![Retro_Left+Middle](images/RetroMouse/Retro_Left+Middle.png)   | 
| ![Retro_Right+Middle](images/RetroMouse/Retro_Right+Middle.png) |

--RetroMouse Table is optional, the table is for cores that have mouse driven device types--

## Compatibility

--Use [(Core name) Core Compatibility List](URL) or make a table--

| Game | Issue |
|------|-------|
|      |       |

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
