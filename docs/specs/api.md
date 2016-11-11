#Libretro API

The Libretro API is a lightweight C-based Application Programming Interface.

Libretro is an API that exposes generic audio/video/input callbacks. A frontend for libretro (such as RetroArch) handles video output, audio output, input and application lifecycle. A libretro core written in portable C or C++ can run seamlessly on many platforms with very little/no porting effort.

While RetroArch is the reference frontend for libretro, several other projects have used the libretro interface to include support for emulators and/or game engines. libretro is completely open and free for anyone to use.


##Purpose

Libretro is a simple API that allows for the creation of games, emulators and multimedia applications.

Popular examples of implementations for this API includes videogame system emulators and game engines, but also more generalized 3D programs. These programs are instantiated as dynamic libraries. We refer to these as "libretro cores".

When you choose to use the libretro API, your program gets turned into a single library file (called a ‘libretro core’). A frontend that supports the libretro API can then load that library file and run the app. The frontend’s responsibility is to provide all the implementation-specific details, such as video/audio/input drivers. The libretro core’s responsibility is solely to provide the main program. You therefore don’t have to worry about writing different video drivers for Direct3D, OpenGL or worrying about catering to all possible input APIs/sound APIs/supporting all known joypads/etc. This is none of your concern at the libretro core implementation level.

Any project that is ported to work with this API can be made to run on ANY libretro frontend. You maintain a single codebase that only deals with the main program, and you then target one single API (libretro) in order to port your program over to multiple platforms at once.

Other projects benefit from the ever-expanding libretro core software library by implementing the libretro API inside their own projects. To this end, project such as XBMC have already begun writing a libretro driver based on the RetroArch reference libretro frontend.

RetroArch is the official reference frontend, and it is available on nearly all modern-day platforms. It is meant to be fast, simple, yet powerful.

Other platform-specific frontends are also available.

##Target use cases

While the most common use case for libretro has been console emulation, it is equally suited as a platform for almost any 2D game.

###Libretro GL

Aside from retro-style games and emulators that depend on software rendering and where you’d typically need nothing more than the ability to render to a framebuffer, the Libretro API also allows you to target OpenGL. This subset of GL functionality (that we call libretro GL) allows you to create libretro ports that use OpenGL as part of their internal rendering. There are two subsets that can be targeted – either OpenGL 2.0 or OpenGL ES 2.0.

From a portability perspective, we highly recommend that you try to target both so that your libretro GL port will work on both mobile and desktop computers.

##Concepts
###RetroPad

###Advantages

Software that targets the libretro API instantly gains access to all of the platforms that have libretro frontends available. That means your game is immediately available to those platforms’ users without worrying about input/audio/video drivers, compatibility issues or the myriad quirks of the underlying host system(s). Likewise, there’s no need to write specialized GUI code for each platform or to use esoteric cross-platform toolkits, like Qt and GTK+.

Furthermore, once your game supports libretro, all of the libretro frontends’ other features come along for free, such as RetroArch’s real-time rewind, lag-concealing netplay, lossless video recording/streaming and cutting-edge post-processing shader support.

Perhaps best of all: libretro is an open specification that is 100% free to implement, with no licensing fees or hidden strings attached. 
