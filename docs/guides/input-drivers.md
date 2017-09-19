# RetroArch Input drivers

## Input drivers for Linux and Lakka
**Note for Linux**: When not in Xorg, using input devices can be more finicky than in X. The main way to access input directly is using the evdev interface found in /dev/input, and optionally the legacy joystick interface in /dev/input/js\*. To discover devices and support hotplugging, libudev is used. When using udev driver, you have to set the keyboard layout/variant yourself. Set the input_keyboard_layout setting for this. See default retroarch.cfg for syntax.

### udev input driver
udev is the newest input driver and uses the evdev joypad API. It supports hotplugging and force feedback (if supported by device). udev reads evdev events directly and supports keyboard callback, mice, and touchpads. 

Supports:
* Multiple simultaneous mice: Yes
* Absolute coordinate mouse devices (Wiimotes, lightguns, etc): Yes

#### Required packages
To use udev, makde sure the libudev and libxkbdcommon are installed. the udev does not depend on Xorg, but it does also depend on X11 keyboard layout files being installed.

#### Setting up udev permissions
Most Linux distributions prevent users from capturing keyboard/mouse information by default. Only root and users in the group "input" are able to access raw input. This is a security feature in case the system is used by multiple users.

The easiest way to gain access to this input is to:

**Step 1:** Add your user to the group "input" with the command: ``sudo usermod -a -G input `whoami` ``
**Step 2:** Log out, and then log back in

If adding your user to the input group does not succeed, you may also set up a udev rule which makes this input accessible to non-root users:

**Step 1:** Add to `/etc/udev/rules.d/99-evdev.rules`:** `KERNEL=="event*", NAME="input/%k", MODE="666"`
**Step 2:** Reload the rules with `sudo udevadm control --reload-rules`.
**Step 3:** Reboot

### linuxraw input driver
An older linuxraw driver is available which uses the older joystick API (/dev/input/js*). The  linuxraw driver requires an active TTY in order to read keyboard events.

Supports:
* Multiple simultaneous mice: Unknown
* Absolute coordinate mouse devices (Wiimotes, lightguns, etc): Yes

### sdl input driver
-To be written-

## Input drivers for Windows

### raw input driver

Supports:
* Multiple simultaneous mice: Yes
* Absolute coordinate mouse devices (Wiimotes, lightguns, etc): Yes

### dinput input driver

Supports:
* Multiple simultaneous mice: No
* Absolute coordinate mouse devices (Wiimotes, lightguns, etc): No

### sdl2 input driver
-To be written-

## Input drivers for Android
-To be written-

## Input drivers for OS X
-To be written-
