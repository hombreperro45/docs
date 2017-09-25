# RetroArch Input drivers

## Input drivers for Linux
The recommended way to access input in Linux is via the `udev` input driver. the `evdev` interface in `/dev/input`. The legacy joystick interface in `/dev/input/js\*` can also be used. 

### udev input driver
udev is the newest input driver and uses the evdev joypad API. It supports hotplugging and force feedback (if supported by device). udev reads evdev events directly and supports keyboard callback, mice, and touchpads. `libudev` is used to discover devices and support hotplugging.

#### Features

| Multi-mouse | Absolute mice* | Rumble | 
|---|---|---|
| Yes |  No | - |

\*Absolute mouse devices include modern lightguns, air mice, Wiimotes, etc.

#### Required packages
TThe `libudev` and `libxkbdcommon` packages are required. udev does not require X, but udev does depend on X11 keyboard layout files being installed.

#### Setting up udev permissions
Most Linux distributions prevent users from capturing keyboard/mouse information by default. Only root and users in the group "input" are able to access raw input. This is a security feature in case the system is used by multiple users.

The easiest way to gain access to this input is to:

* **Step 1:** Add your user to the group "input" with the command: ``sudo usermod -a -G input `whoami` ``
* **Step 2:** Log out, and then log back in

If adding your user to the input group does not succeed, you may also set up a udev rule which makes this input accessible to non-root users:

* **Step 1:** Add to `/etc/udev/rules.d/99-evdev.rules`:** `KERNEL=="event*", NAME="input/%k", MODE="666"`
* **Step 2:** Reload the rules with `sudo udevadm control --reload-rules`.
* **Step 3:** Reboot

### linuxraw input driver
The older linuxraw driver is available which uses the legacy joystick API at `/dev/input/js*`. The  linuxraw driver requires an active TTY in order to read keyboard events.

#### Features

| Multi-mouse | Absolute mice* | Rumble | 
|---|---|---|
| -           |  Yes           |   -    |

\*Absolute mouse devices include modern lightguns, air mice, Wiimotes, etc.

### wayland input driver
-To be written-

#### Features

| Multi-mouse | Absolute mice* | Rumble | 
|---|---|---|
| -           |  -             |   -    |

\*Absolute mouse devices include modern lightguns, air mice, Wiimotes, etc.
### sdl input driver
-To be written-

#### Features

| Multi-mouse | Absolute mice* | Rumble | 
|---|---|---|
| -           |  -             |   -    |

\*Absolute mouse devices include modern lightguns, air mice, Wiimotes, etc.

---

## Input drivers for Windows

### raw input driver

#### Features

| Multi-mouse | Absolute mice* | Rumble | 
|---|---|---|
| Yes         |  Yes           |   -    |

\*Absolute mouse devices include modern lightguns, air mice, Wiimotes, etc.

### dinput input driver

#### Features

| Multi-mouse | Absolute mice* | Rumble | 
|---|---|---|
| No          |  No            |   -    |

\*Absolute mouse devices include modern lightguns, air mice, Wiimotes, etc.

### sdl2 input driver
-To be written-

#### Features

| Multi-mouse | Absolute mice* | Rumble | 
|---|---|---|
| -           |  -             |   -    |

\*Absolute mouse devices include modern lightguns, air mice, Wiimotes, etc.

---

## android input driver
-To be written-

#### Features

| Multi-mouse | Absolute mice* | Rumble | 
|---|---|---|
| -           |  -             |   -    |

\*Absolute mouse devices include modern lightguns, air mice, Wiimotes, etc.

## Input drivers for OS X
-To be written-

### cocoa input driver
-To be written-

#### Features

| Multi-mouse | Absolute mice* | Rumble | 
|---|---|---|
| -           |  -             |   -    |

\*Absolute mouse devices include modern lightguns, air mice, Wiimotes, etc.

---

## DOS input driver
-To be written-

#### Features

| Multi-mouse | Absolute mice* | Rumble | 
|---|---|---|
| -           |  -             |   -    |

\*Absolute mouse devices include modern lightguns, air mice, Wiimotes, etc.
