# RetroArch Input drivers

## Input drivers for Linux and Lakka
*Note: When not in Xorg, using input devices can be more finicky than in X. The main way to access input directly is using the evdev interface found in /dev/input, and optionally the legacy joystick interface in /dev/input/js\*. To discover devices and support hotplugging, libudev is used.*

### dev/evdev input drivers
To use udev/evdev drivers, RetroArch depends on the libudev package. To support keyboard callback interface in udev, the libxkbcommon package (version 0.3 and up) is required. It is used to translate raw evdev events to printable characters. It does not depend on Xorg, but it depends on X11 keyboard layout files being installed.

#### Setting up udev permissions
By default in most distros, /dev/input nodes are root-only (mode 600). You can set up a udev rule which makes these accessible to non-root.

**Add to `/etc/udev/rules.d/99-evdev.rules`:** `KERNEL=="event*", NAME="input/%k", MODE="666"`

Then reload rules with `sudo udevadm control --reload-rules`.
Until next reboot (or replugging devices), you can force permissions with `sudo chmod 666 /dev/input/event*`.

#### Keyboard/mouse/touchpad
RetroArch has two drivers for keyboard which can run without X. udev is a newer driver which reads evdev events directly. It also supports keyboard callback, mice and touchpads. The older linuxraw driver requires an active TTY. Keyboard events are read directly from the TTY which makes it simpler, but not as flexible. Mice, etc, are not supported at all.

udev is preferred over linuxraw when applicable.

#### Configuring keyboard layout for udev/evdev keyboard
When using udev driver, you have to set the keyboard layout/variant yourself. Set the input_keyboard_layout setting for this. See default retroarch.cfg for syntax.

#### Joypads
RetroArch has three drivers for joypads on Linux. udev is a newer driver which uses the recent evdev joypad API. It supports hotplugging and force feedback (if supported by device). An older linuxraw driver is also supported, which uses the older joystick API (/dev/input/js*). Finally, SDL driver can be used.

udev is the default driver for joypads.

## Input drivers for Windows

### raw input driver

## Input drivers for OS X

To be written
