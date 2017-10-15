# 3D Engine

## Background

3D Engine for libretro GL with additional features (camera/location/etc); a tech demo.

Author(s):

Team Libretro

## Contribute to this documentation

In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/library/3d_engine.md). Changes are proposed using "Pull Requests."

## License

GPLv3

## Extensions

png|jpg|mtl|obj

## BIOS

The 3D Engine core does not feature BIOS use.

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
| Controllers       | ✕         |
| Multi-Mouse       | ✕         |
| Rumble            | ✕         |
| Sensors           | ✔         |
| Camera            | ✔         |
| Location          | ✔         |
| Subsystem         | ✕         |

The 3D Engine core creates directories named 'Libretro 3DEngine' in RetroArch's save and state directories

## Options

The 3D Engine core has the following options that can be tweaked from the core options menu. The default setting is bolded.

- **Internal resolution** (**320x240**/360x480/480x272/512x384/512x512/640x240/640x448/640x480/720x576/800x600/960x720/1024x768): Self-explanatory.
- **Cube size** (**0**/1/2/4/8/16/32/64/128): Awaiting description.
- **Cube stride** (2.0/3.0/4.0/5.0/6.0/7.0/8.0): Awaiting description.
- **Camera enable** (**Off**/On): Awaiting description.
- **Camera FB Type** (**texture**/raw framebuffer): Awaiting description.
- **Sensor enable** (**Off**/On): Awaiting description.
- **Location enable** (**Off**/On): Awaiting description.
- **Location camera control** (**Off**/On): Awaiting description.
- **Discard hack enable** (**Off**/On): Awaiting description.
- **Location position OSD** (**Off**/On): Awaiting description.

## Controllers

The 3D Engine core supports 2 controller setting(s), the bolded controller setting is default:

* **RetroPad** - [Joypad without analog]

* **RetroPad w/Analog** - [Joypad with analog]

## Compatibility

The 3D Engine core does not have specific compatiblity issues

## External Links

* [Libretro Repository](https://github.com/libretro/libretro-3dengine)
* [Report Core Issues Here](https://github.com/libretro/libretro-meta)