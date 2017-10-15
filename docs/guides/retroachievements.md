# RetroAchievements In RetroArch

## **What are RetroAchievements?**

[retroachievements.org](http://www.retroachievements.org/) is a service that provides a trophies unlocking mechanism similar to modern consoles, for Retro games.

!!! Warning
    The service is not maintained by RetroArch or the Libretro team.


## **How to setup achievements**

1. Register an account on [retroachievements.org](http://www.retroachievements.org/)
2. Enable the functionality and fill your retroachievements credentials in Settings->Achievements.

!!! note 
	The hardcore mode prevents you from using emulation features like slow motion, fast forwarding, cheats and savestates.
	**BUT** gives you double points.

![Settings](../guides/images/retroachievements/achievements-settings.png)

## **Check your connection to the service**

**You need an active Internet connection.**

In this example, we are using the game Chrono Trigger (USA) with the core snes9x.

Launch the game and trigger the Quick Menu.

Go to Achievements and you should see a list of the unlockable trophies for this game.

![List](../guides/images/retroachievements/achievements-list.png)


## **Check your progress**

On the retroachievements website, you can login and access your account page.

You should be able to check your progress in the games and see which trophies you unlocked.

Trophies unlocked in hardcore mode are marked with a special color.

You can also check the progress of your friends and add comments on their trophies.

![Progress](../guides/images/retroachievements/achievements-progress.png)


## **Cores Compatibility** (15 of october 2017)

### NES

| Core				                                                		| Supported | Notes |
|---------------------------------------------------------------------------|:---------:|-------|
| [QuickNES](https://github.com/libretro/QuickNES_Core)             		| ✔         | On Android has a [known issue](https://github.com/libretro/RetroArch/issues/3973)|
| [FCEUmm](https://github.com/libretro/libretro-fceumm)             		| ✔         |		|
| [Nestopia UE](https://github.com/libretro/nestopia)						| ✕         |		|
| [bnes](https://github.com/libretro/bnes-libretro)							| ✕         |		|
| [Emux](https://github.com/libretro/emux)									| ✕         |		|

### Master System / MegaDrive - Genesis

| Core				                                                		| Supported |
|---------------------------------------------------------------------------|:---------:|
| [Genesis Plus GX](https://github.com/libretro/Genesis-Plus-GX)			| ✔         |
| [picodrive](https://github.com/libretro/picodrive)						| ✔         |
| [Emux](https://github.com/libretro/emux)									| ✕         |

### SNES

| Core				                                                		| Supported | Notes |
|---------------------------------------------------------------------------|:---------:|-------|
| [Snes9x 2010](https://github.com/libretro/snes9x2010)						| ✔         | *Previously called SNES9x Next*	|
| [Snes9x 2005](https://github.com/libretro/snes9x2005)						| ✔         | *Previously called CAT SFC*		|
| [Snes9x 2002](https://github.com/libretro/snes9x2002)						| ✔         | *Previously called PocketSNES*	|
| [Snes9x](https://github.com/libretro/snes9x)								| ✔         | **Partially Supported**			|
| [bsnes](https://github.com/libretro/bsnes-libretro)						| ✔         |		|
| [bsnes-mercury](https://github.com/libretro/bsnes-mercury)				| ✔         |		|
| [Beetle bsnes](https://github.com/libretro/beetle-bsnes-libretro)			| ?         |		|

### Game Boy / Game Boy Color

| Core					                                                	| Supported | Notes |
|---------------------------------------------------------------------------|:---------:|-------|
| [gambatte](https://github.com/libretro/gambatte-libretro)					| ✔         |		|
| [mGBA](https://github.com/libretro/mgba)									| ✕         | Achievements only work for Game boy Advance |
| [Emux](https://github.com/libretro/emux)									| ✕         |		|
| [SameBoy](https://github.com/libretro/SameBoy)							| ✕         |		|
| [TGB Dual](https://github.com/libretro/tgbdual-libretro)					| ✕         |		|

### Game Boy Advance

| Core					                                                	| Supported |
|---------------------------------------------------------------------------|:---------:|
| [mGBA](https://github.com/libretro/mgba)									| ✔         |
| [VBA next](https://github.com/libretro/vba-next)							| ✔         |
| [VBA-M](https://github.com/libretro/vbam-libretro)						| ✔         |
| [Beetle GBA](https://github.com/libretro/beetle-gba-libretro)				| ✕         |
| [gpSP](https://github.com/libretro/gpsp)									| ✕         |
| [Meteor](https://github.com/libretro/meteor-libretro)						| ✕         |

### PC Engine

| Core					                                                	| Supported |
|---------------------------------------------------------------------------|:---------:|
| [Beetle PCE Fast](https://github.com/libretro/beetle-pce-fast-libretro)	| ✔         |


### Nintendo 64

| Core					                                                	| Supported |
|---------------------------------------------------------------------------|:---------:|
| [Mupen 64 plus](https://github.com/libretro/mupen64plus-libretro)			| ✔         |
| [Parallel N64](https://github.com/libretro/parallel-n64)					| ✔         |


!!! Note
	If you want to contribute, please update RetroArch and cores to get the latest fixes on the RetroAchievements feature;
    then in order to propose improvements to this document, [do it via github](https://github.com/libretro/docs/tree/master/docs/guides/retroachievements.md) using "Pull Requests"


