# RetroAchievements In RetroArch

## What are RetroAchievements?

http://retroachievements.org is a service to provide a trophies unlocking mechanism similar to modern web consoles for Retro games.

It has been integrated into RetroArch.

!!! warning
    The service is not maintained by RetroArch or the Libretro team.

## Get Set Up

Follow this [Quick Guide](http://www.retroarch.com/index.php?page=achievements) to get them activated in RetroArch.

## Compatible Cores

This is an attempt to make a compatibility list of libretro cores and RetroAchievements. If you want to contribute, please, update your RetroArch and cores to get the latest fixes on the RetroAchievements feature.

**Full details below the list.**

!!! tip
    +In order to propose improvements to this document, [visit it's corresponding source page on github](https://github.com/libretro/docs/tree/master/docs/guides/retroachievements.md). Changes are proposed using "Pull Requests."

### NES

* QuickNES
* FCEUmm
* Nestopia

### MegaDrive / Genesis

* picodrive
* Genesis Plus GX

### SNES

* Snes9x 2010
* Snes9x 2005
* Snes9x 2002
* Snes9x

### Game Boy / Game Boy Color

* gambatte
* mGBA

### Game Boy Advance

* mGBA
* VBA Next
* VBA-M

### PC Engine

* Beetle PCE Fast

### Master System

* picodrive
* Genesis Plus GX

### Nintendo 64

* Mupen 64 plus
* Parallel N64

## Recommended Cores


* **NES:** FCEUmm and QuickNES
* **Mega Drive / Genesis:** Genesis Plus GX and picodrive
* **SNES:** Snes9x 2010
* **Game Boy / Game Boy Color:** gambatte
* **Game Boy Advance:** mGBA and VBA-M
* **PC Engine:** Beetle PCE Fast
* **Master System:** Genesis Plus GX and picodrive
* **Nintendo 64:** Mupen 64 plus and Parallel N64

## Core Specific details

### NES

#### QuickNES

[from this repository](https://github.com/libretro/QuickNES_Core)

**Works.**

!!! note
    There's a [known issue](https://github.com/libretro/RetroArch/issues/3973) with QuickNES on Android (not related to RetroAchievements); in the impossibility of using QuickNES it is recommended to use FCEUmm).

#### FCEUmm

[from this repository](https://github.com/libretro/libretro-fceumm)

**Works.**

#### Nestopia

[from this repository](https://github.com/libretro/nestopia)

**Doesn't work.**

### MegaDrive/Genesis

#### picodrive

[from this repository](https://github.com/libretro/picodrive)

**Works.**

#### Genesis Plus GX

[from this repository](https://github.com/libretro/Genesis-Plus-GX)

**Works.**

### SNES

#### Snes9x 2010

previously called SNES9x Next, [from this repository](https://github.com/libretro/snes9x2010)

**Works.**

#### Snes9x 2005

previously called CAT SFC, [from this repository](https://github.com/libretro/snes9x2005)

**Untested.**

#### Snes9x 2002

previously called PocketSNES, [from this repository](https://github.com/libretro/snes9x2002)

**Works.**

#### Snes9x

[from this repository](https://github.com/libretro/snes9x)

**Partially Supported**

### Game Boy/Game Boy Color

#### gambatte

[from this repository](https://github.com/libretro/gambatte-libretro)

**Works.**

#### mGBA

[from this repository](https://github.com/libretro/mgba)

Although mGBA can play Game Boy/Game Boy Color ROMs, it does NOT support cheevos for these systems (only for Game Boy Advance).

### Game Boy Advance

#### mGBA

[from this repository](https://github.com/libretro/mgba)

**Works.**

#### VBA next

[from this repository](https://github.com/libretro/vba-next)

**Doesn't work OK.**

"vba-next doesn't support the memory map interface, so achievements won't work ok with it." - @leiradel

#### VBA-M

[from this repository](https://github.com/libretro/vbam-libretro)

**Seems to be working fine, but need more tests.**

### PC Engine

#### Beetle PCE Fast

[from this repositor](https://github.com/libretro/beetle-pce-fast-libretro)

**Works.**

### Master System

In April 2017 RetroAchievements.org people started to add some cheevos for Sega Master System.

#### picodrive

[from this repository](https://github.com/libretro/picodrive)

It seems to be working fine after the fix picodrive received in 18-April-2017.

**Works.**

#### Genesis Plus GX

[from this repository](https://github.com/libretro/Genesis-Plus-GX)

**Works.**

### Nintendo 64

In April 2017 RetroAchievements.org people started to add some cheevos for Nintendo 64.

#### Mupen 64 plus

[from this repository](https://github.com/libretro/mupen64plus-libretro)

This core got a fix in 8-July-2017 and seems to be working fine with cheevos.

**Works.**

#### Parallel N64

[from this repository](https://github.com/libretro/parallel-n64)

This core got a fix in 8-July-2017 and seems to be working fine with cheevos.

**Works.**
