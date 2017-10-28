# Dinothawr

## Background

Dinothawr is a block pushing puzzle game on slippery surfaces. Our hero is a dinosaur whose friends are trapped in ice. Through puzzles it is your task to free the dinos from their ice prison.

### Author(s):

Themaister|Agnes Heyer

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/dinothawr.md). Changes are proposed using "Pull Requests."

## License

Non-commercial

## Extensions

*Content that can be loaded by the Dinothawr core have the following file extensions.*

game

## Database(s)

*RetroArch databases that are associated with the Dinothawr core*

* Dinothawr

## BIOS

**How to get and install this:**

1. Start up RetroArch. Inside the main menu, go to 'Online Updater'.

2. Just to make sure we have the latest info files, select 'Update Core Info FIles'. Wait until this is done. Then, select 'Core Updater'.

3. Browse through the list and select 'Dinothawr'.

4. After this has finished downloading, you now need to obtain Dinothawr's data files. You can do this by going back to the previous menu screen. From there, select 'Content Downloader'.

5. Select 'Dinothawr', then select 'Dinothawr.zip'. This should download and extract this file to RetroArch's Downloads directory.

**How to play (after installation):**

1. Go back to RetroArch's main menu screen. Select 'Load Content', then 'Downloads'.

2. Select the 'dinothawr' directory, then select 'dinothawr.game'.

3. If you are asked which core to select, choose 'Dinothawr'.

The game should now start running!

|   Filename     |    Description                 |              md5sum              |
|:--------------:|:------------------------------:|:--------------------------------:|
| dinothawr.game | Dinothawr game file - Required | a8db0d14628759a5ebafb420e05105bf |

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
| Controllers       | ✓         |
| Multi-Mouse       | ✕         |
| Rumble            | ✕         |
| Sensors           | ✕         |
| Camera            | ✕         |
| Location          | ✕         |
| Subsystem         | ✕         |

The Dinothawr core creates directories named 'Dinothawr' in RetroArch's...

* Savefile directory when the core is loaded.
* Statestate directory when the core is loaded.
* Config directory when a Core Override or a Game Override or a Game-options file is saved.
* Input Remapping directory when a Core Remap or a Game Remap is saved.
* Shaders Presets directory when a Core Preset or a Game Preset is saved.

Core Overrides/Remaps/Presets that are saved will be named 'Dinothawr'.

Game Overrides/Remaps/Presets and Game-option files will have the same name as the loaded content.

Game data is saved/loaded to and from 'dinothawr.srm' in the core's save directory 

## Options

*The Dinothawr core has the following option(s) that can be tweaked from the core options menu. The default setting is bolded.*

- **Timer as FPS reference** (Off/**On**): Use timer as FPS reference.

## Controllers

*The Dinothawr core supports the following controller setting(s), bolded controller settings are the default for the specified user(s):*

### User 1 - 16 Device Type(s)

* **RetroPad** - Joypad without analog

* RetroPad w/Analog - Joypad with analog

### Controllers graph

| Dinothawr   | RetroPad                                                       |
|-------------|----------------------------------------------------------------|
| Push        | ![RetroPad_B](images/RetroPad/Retro_B_Round.png)               |
| D-Pad Up    | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Up.png)            |
| D-Pad Down  | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Down.png)          |
| D-Pad Left  | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Left.png)          |
| D-Pad Right | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad_Right.png)         |
| Menu        | ![RetroPad_A](images/RetroPad/Retro_A_Round.png)               |
| Reset       | ![RetroPad_X](images/RetroPad/Retro_X_Round.png)               |

## Customizing / Hacking

Dinothawr is fairly hackable. dinothawr.game is the game file itself. It is a simple XML file which points to all assets used by the game. Levels are organized in chapters. Levels themselves are created using the [Tiled](http://www.mapeditor.org/) editor. If you want to try making your own levels, make sure you use the "plain XML" format for .tmx files and not the default zlib base64.

[Dinothawr - Level Design guide (pdf)](http://retinaleclipse.com/dinothawr-guide.pdf)

## External Links

* [Official Repository](https://github.com/libretro/Dinothawr)
* [Report Core Issues Here](https://github.com/libretro/libretro-meta)