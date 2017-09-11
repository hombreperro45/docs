# Understanding RetroArch Settings Systems

There are various and comprehensive ways to save customized settings within the RetroArch menus. All the settings files are plain text and can be adjusted manually with a text editor.

- Global settings can be overridden on a per core or per game basis, with the config override system.
- Input settings are handled separately with the input core and game Remap system.
- Likewise Shader settings are also their own entity for per core and per game settings
- A standalone file also saves the Option settings for all cores that support them. The settings is this file can be overridden on a per game basis.

!!! tip
    Please read the [Getting Started](guides/windows.md) guide.

## Hierarchy

### Options

1. Game options
2. Core options

### Configurations

1. Game Overrides
2. Core Overrides
3. Main Configurations

### Inputs

1. Game Remap
2. Core Remap
3. Main User Binds

### Shaders

1. Game Preset
2. Core Preset

## Configuartion Files

!!! note
    Depending on your chosen platform the location of these files after installation may vary.

!!! warning
    Some settings cannot be saved in an override file from the menu. Full details found below. You can manually add settings to the override file to workaround most situations.


**The default and global settings file**

- retroarch.cfg  (located in the base install path)

**The global file for core option settings, for cores that support options**

- retroarch-core-options.cfg (located with the retroarch.cfg)

### Core options

- "name-of-game.opt" **If not found load**
    - retroarch-core-options.cfg

The options files list the settings found under `Quick Menu->Options`. The `retroarch-core-options.cfg` is created automatically on loading a core that supports Options.
A game specific options file is created when you select `Quick Menu->Options->Game-options file`. (located in "corename" directory, at the path set under `Settings->Directory->Config`)

### Override Configs

The override system activates on loading of content. RetroArch looks for configs with this logic.

#### Per Core/Game Overrides

- "name-of-game".cfg **If not found load**
    - "name-of-core".cfg **If not found load**
        - retroarch.cfg

**Per Core Override**

- "name-of-core".cfg (located in "corename" directory, at the path set under `Settings->Directory->Config`)

These settings files are created from the `Quick Menu->Save Core Overrides` option and contain ANY (supported) settings you have changed since loading content.    

**Per Game Override**

- "name-of-game".cfg (located with per core override file)

These settings files are created as above with the `Quick Menu->Save Game Overrides`. The settings will take precedence over "name-of-core".cfg

### Input Remaps

To be written

### Shader Presets

To be written
