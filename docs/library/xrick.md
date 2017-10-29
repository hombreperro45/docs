# Rick Dangerous (XRick)

## Background

Xrick is an open source implementation of the game "Rick Dangerous".

This libretro core is based on BigOrno's [work](http://www.bigorno.net/xrick/).

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/xrick.md). Changes are proposed using "Pull Requests."

## License

GPLv3

## Extensions

*Content that can be loaded by the XRick core have the following file extensions.*

zip

## Database(s)

*RetroArch databases that are associated with the XRick core*

* Rick Dangerous

## BIOS

**How to get and install this:**

1. Start up RetroArch. Inside the main menu, go to 'Online Updater'.

2. Just to make sure we have the latest info files, select 'Update Core Info FIles'. Wait until this is done. Then, select 'Core Updater'.

3. Browse through the list and select 'Rick Dangerous (XRick)'.

4. After this has finished downloading, you now need to obtain the Rick Dangerous' data files. You can do this by going back to the previous menu screen. From there, select 'Content Downloader'.

5. Select 'Rick Dangerous', then select 'Rick Dangerous.zip'. This should download and extract this file to RetroArch's Downloads directory.

**How to play (after installation):**

1. Go back to RetroArch's main menu screen. Select 'Load Content', then 'Downloads'.

2. Select the 'xrick' directory, then select 'data.zip'.

3.  Select 'Load Archive'. If you are asked which core to select, choose 'Rick Dangerous (Xrick)'.

The game should now start running!

|   Filename    |    Description         |              md5sum              |
|:-------------:|:----------------------:|:--------------------------------:|
| data.zip      | Rick Dangerous game data folder - Required | a471e64e9f69afbe59c10cc94ed1b184 |

## Features

| Feature           | Supported |
|-------------------|:---------:|
| Saves             | ✕         |
| States            | ✕         |
| Rewind            | ✕         |
| Netplay           | ✕         |
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

The XRick core creates directories named 'xrick' in RetroArch's...

* Savefile directory when the core is loaded.
* Statestate directory when the core is loaded.
* Config directory when a Core Override or a Game Override or a Game-options file is saved.
* Input Remapping directory when a Core Remap or a Game Remap is saved.
* Shaders Presets directory when a Core Preset or a Game Preset is saved.

Core Overrides/Remaps/Presets that are saved will be named 'xrick'.

Game Overrides/Remaps/Presets and Game-option files will have the same name as the loaded content.

## Options

The XRick core does not feature core options.

## Controllers

*The XRick core supports the following controller setting(s), bolded controller settings are the default for the specified user(s):*

### User 1 - 16 Device Type(s)

* **RetroPad** - Joypad without analog 

* RetroPad w/Analog - Joypad with analog

### Controllers graph

| XRick     | RetroPad                                                       |
|-----------|----------------------------------------------------------------|
| Jump      | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Up.png)            |
| Crouch    | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Down.png)          |
| Left      | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Left.png)          |
| Right     | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Right.png)         |
| Attack†  | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)                |

† Press and hold this button, then press left or right to stab using your bayonet. If you press and hold the button and then press Up, you can shoot at an enemy. If you press and hold the button and then press Down instead, you will drop a bomb which will detonate after some time.

## External Links

* [Libretro Repository](https://github.com/libretro/xrick-libretro)
* [Report Core Issues Here](https://github.com/libretro/libretro-meta)
* [Official Website](http://www.bigorno.net/xrick/)