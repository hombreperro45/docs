# RetroArch Input drivers

## Input drivers for Linux and Lakka
**Note for Linux**: When not in Xorg, using input devices can be more finicky than in X. The main way to access input directly is using the evdev interface found in /dev/input, and optionally the legacy joystick interface in /dev/input/js\*. To discover devices and support hotplugging, libudev is used. When using udev driver, you have to set the keyboard layout/variant yourself. Set the input_keyboard_layout setting for this. See default retroarch.cfg for syntax.

### udev/evdev input drivers
udev is the newest input driver and uses the recent evdev joypad API. It supports hotplugging and force feedback (if supported by device). udev reads evdev events directly and supports keyboard callback, mice, and touchpads. 

udev is currently the only Linux input driver with support for multiple simultaneous mouse devices.

To use udev/evdev drivers, RetroArch depends on the libudev package. To support keyboard callback interface in udev, the libxkbcommon package (version 0.3 and up) is required. It is used to translate raw evdev events to printable characters. It does not depend on Xorg, but it depends on X11 keyboard layout files being installed.

#### Setting up udev permissions
By default in most distros, /dev/input nodes are root-only (mode 600). You can set up a udev rule which makes these accessible to non-root.

**Add to `/etc/udev/rules.d/99-evdev.rules`:** `KERNEL=="event*", NAME="input/%k", MODE="666"`

Then reload rules with `sudo udevadm control --reload-rules`.
Until next reboot (or replugging devices), you can force permissions with `sudo chmod 666 /dev/input/event*`.

### linuxraw input driver
An older linuxraw driver is available which uses the older joystick API (/dev/input/js*). The  linuxraw driver requires an active TTY. Keyboard events are read directly from the TTY which makes it simpler, but not as flexible. Mice, etc, are not supported.

### sdl input driver
-To be written-

## Input drivers for Windows

### raw input driver
The `raw` input driver is currently the only Windows input driver with support for multiple simultaneous mice. It is also the only Windows input driver with support for 'absolute coordinate' mouse devices, such as the Wiimote/Dolphinbar and non-CRT lightguns.

### dinput input driver
-To be written-

### sdl2 input driver
-To be written-

## Input drivers for OS X
-To be written-
