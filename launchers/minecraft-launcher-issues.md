---
description: Most issues are simple and can be easily fixed within the launcher.
---

# Minecraft Launcher Issues

## TL;DR

* Restart the launcher
* Make sure you've launched a vanilla 1.8.9 Minecraft instance
* Restart your game
* Manually create a new instance
* If all else fails; use Prism Launcher

## Easy Fixes

### Create a new 1.8.9 instance

`Unable to locate game files. Filename on disk: 1.8.9.jar`

Create and launch a `Vanilla 1.8.9` instance if you haven't already. Then, try launching your SkyClient or Forge instance again.

### Restart your game

`Invalid Session - Failed to login`

The best solution is to re-login to your launcher and relaunch the game. Occasionally, this issue can be remedied using Essential's account switcher. However, this isn't recommended as it can cause other issues.

### SkyClient installation not showing in the launcher

There's a few reasons which could cause this issue, try the steps below in order

**Version:** 1.8.9-forge1.8.9-11.15.1.2318-1.8.9

1. Close and reopen the launcher
2. Open the `Installations` tab and press `New installation`. Set the version to the one listed above. (This should be one of the last options)
3. See below for setting the `Game Directory`

<details>

<summary>Game directories</summary>

**For Windows users:**

* `C:/Users/YOUR_PC_LOGIN_NAME/AppData/Roaming/.minecraft/skyclient`

**For MacOS/OSX users:**

* `~/Library/Application Support/minecraft/skyclient`

**For Linux users:**

Change if they are using flatpak's MC launcher

* `~/.minecraft/skyclient`

</details>

The launcher has a weird way of handling and storing profiles, and sometimes, when the installer tries to edit the profiles, it just does not work or update.

## Not so easy fixes

A list of fixes that don't have easy or known fixes. See the section below for how to fix these.

* "Unable to start Minecraft" with literally no other explanation.
* "Unable to extract native files" or download any other of the game's libraries. May be possible to work around via VPN or manually installation. Alternatively you could just share the files you have on your PC, but these fixes suck.

## If all else fails, use Prism Launcher

The official launcher is messy and some issues cannot be fixed. We suggest switching to [Prism Launcher](https://prismlauncher.org/), an open-sourced launcher alternative. Microcontrollers has an [advanced guide](https://microcontrollersdev.github.io/Alternatives/launcher/home/) to setting up Prism which may be a bit complicated for regular users.
