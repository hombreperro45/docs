# 3DO (4DO)

## Background

4DO is an open-source, low-level emulator for the 3DO Game Console based on the FreeDO source code.

## License

Non-commercial

## Extensions

iso|cue

## BIOS

|   Filename   |      Description     |              md5sum              |
|:------------:|:--------------------:|:--------------------------------:|
| panafz10.bin | Panasonic FZ-10 BIOS | 51f2f43ae2f3508a14d9f56597e2d3ce |

## Feature Support

These are libretro features, not frontend or standalone emulator features.

| Saves | Save states | Rewind | Netplay | RetroAchievements | Cheats | Controllers API | Rumble | Sensors | Camera | Location | Subsystem API |
|:-----:|:-----------:|:------:|:-------:|:-----------------:|:------:|:---------------:|:------:|:-------:|:------:|:--------:|:-------------:|
|  yes  |     yes     |   yes  |   yes   |         no        |   no   |        no       |   no   |    no   |   no   |    no    |       no      |

## Options

|   Core Option   |         Description         | Options (Default Bolded) | Requires Restart |
|:---------------:|:---------------------------:|:------------------------:|:----------------:|
| High Resolution | Doubles internal resolution |        **Off**/On        |        Yes       |

## Controllers

The core supports one controller setting:
* Joypad: Controller

|                      [RetroPad](RetroPad)                      |   3do Joypad   |
|:--------------------------------------------------------------:|:--------------:|
|        ![RetroPad_A](images/RetroPad/Retro_A_Round.png)        |        C       |
|        ![RetroPad_B](images/RetroPad/Retro_B_Round.png)        |        B       |
|        ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)        |      D-pad     |
|          ![RetroPad_L1](images/RetroPad/Retro_L1.png)          |  Left Shoulder |
|          ![RetroPad_L2](images/RetroPad/Retro_L2.png)          |                |
|          ![RetroPad_L3](images/RetroPad/Retro_L3.png)          |                |
|  ![RetroPad_Left_Stick](images/RetroPad/Retro_Left_Stick.png)  |                |
|          ![RetroPad_R1](images/RetroPad/Retro_R1.png)          | Right Shoulder |
|          ![RetroPad_R2](images/RetroPad/Retro_R2.png)          |                |
|          ![RetroPad_R3](images/RetroPad/Retro_R3.png)          |                |
| ![RetroPad_Right_Stick](images/RetroPad/Retro_Right_Stick.png) |                |
|      ![RetroPad_Select](images/RetroPad/Retro_Select.png)      |      Stop      |
|       ![RetroPad_Start](images/RetroPad/Retro_Start.png)       |   Play/Pause   |
|        ![RetroPad_X](images/RetroPad/Retro_X_Round.png)        |                |
|        ![RetroPad_Y](images/RetroPad/Retro_Y_Round.png)        |        A       |

![3do_joypad_diagram](https://cloud.githubusercontent.com/assets/10035308/16599643/7f450bd6-42c0-11e6-84d7-9cc0944e7b01.png)

## External Links

* Official Website: [http://www.fourdo.com/](http://www.fourdo.com/) 
* Libretro Repository: [https://github.com/libretro/4do-libretro](https://github.com/libretro/4do-libretro)
