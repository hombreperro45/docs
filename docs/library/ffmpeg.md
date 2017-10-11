# FFmpeg

## Background

Video/music player implemented in libretro.

Author(s): Fabrice Bellard|FFmpeg team

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/ffmpeg.md). Changes are proposed using "Pull Requests."

## License

LGPLv2, GPLv2

## Extensions

mkv|avi|f4v|f4f|3gp|ogm|flv|mp4|mp3|flac|ogg|m4a|webm|3g2|mov|wmv|mpg|mpeg|vob|asf|divx|m2p|m2ts|ps|ts|mxf|wma|wav

## BIOS

The FFmpeg core does not feature BIOS use.

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

## Options

The FFmpeg core has the following options that can be tweaked from the core options menu. The default setting is bolded.

- **Temporal Interpolation** (**On**/Off): 'Fake’ a higher framerate through by using motion blur
- **FFT Resolution** (**1280x720**/1920x1080/2560x1440/3840x2160/640x360/320x180): Awaiting description.
- **FFT Multisample** (**1x**/2x/4x): Awaiting description.
- **Colorspace** (**auto**/BT.709/BT.601/FCC/SMPTE240M): Awaiting description.

## Controllers

The FFmpeg core supports 1 controller setting(s):

* RetroPad

![retropad](images/controllers/ffmpeg_retropad.png)

| FFmpeg    | [RetroPad](RetroPad)                                            |
|-----------|----------------------------------------------------------------|
| Seek +/- 10/60 seconds | ![RetroPad_Dpad](images/RetroPad/Retro_Dpad.png)  |
| Cycle Audio Track      | ![RetroPad_L1](images/RetroPad/Retro_L1.png)      |
| Cycle Subtitle Track   | ![RetroPad_R1](images/RetroPad/Retro_R1.png)      |


## Compatibility

The FFmpeg core does not have specific compatiblity issues

## External Links

* [Libretro Repository](https://github.com/libretro/FFmpeg)
* [Report Core Issues Here](https://github.com/libretro/libretro-meta)
* [Official Website](https://www.ffmpeg.org/)
* [Github mirror of Main FFmpeg Git repository](https://github.com/FFmpeg/FFmpeg)