---
description: Issues with Prism Launcher. Most of these are user error.
---

# Prism Launcher Issues

## TL;DR

* Install or check if Java is installed
* Make sure Prism is using the correct Java installation&#x20;

***

## The Java binary couldn't be found

For a far more detailed & advanced version, refer to Step 1 in [Microcontroller's guide](https://microcontrollersdev.github.io/Alternatives/launcher/prism\_win/#step-1-installing-java)

### Ensure Java is correctly installed

Many people may forget or incorrectly install Java which means Prism Launcher has no way to launch the game. Check the guide listed below:

* Go to the [Adoptium download page](https://adoptium.net/temurin/releases) or the [Azul Zulu download page](https://www.azul.com/downloads/) (only if you use an M1 or M2 CPU). These are all free and open-source Java installations.
* Set the following:
  * Operating System: Whatever operating system is being used
  * Architecture: x64 or ARM (You need Zulu for macOS ARM)
  * Package Type / Java Package: JDK
  * Version: 8
* Choose the first download (should be a `.msi` for Windows, `.pkg` or `.dmg` for macOS)
* Once downloaded, run and follow the installer process.
* When done, repeat instructions, but set Version to 17.

### Configure instance settings

Even if the correct Java version is installed, Prism may not be configured to use that one.

* Open instance settings by **right-clicking** and pressing `Edit`
* Click `Settings`, and make sure the `Java installation` checkbox is selected
* Press `auto-detect`, and have them choose the `1.8.0_xxx` version of Java
  * The path should look something like `C:/Program Files/Eclipse...`
* If the Java version doesn't appear, completely restart Prism Launcher and try again. Prism only detects binaries on startup

Occasionally, Prism's auto-detect can fail. In these cases, the binary needs to be imported manually

* Open the same `Java settings` tab, but instead, press `Browse`
* Select the correct path, which can change depending on the operating system, or if the user manually changed it. In the end, you're looking for a `javaw`

<details>

<summary>OS file paths</summary>

**Windows:**

* `C:/Program Files/Eclipse Adoptium/jdk-1.8(and then other numbers)-hotspot/bin/javaw.exe`

**MacOS/OSX:**

* `/Library/Java/JavaVirtualMachines/temurin-8.jdk/Contents/Home/bin/java` OR `~/Library/Java/JavaVirtualMachines/temurin-8(and then other numbers)/Home/bin/java`

**Linux:**

Depends on many factors, but it should include either the word `Adoptium`, `Temurin`, `1.8` or `8` in it.

</details>

***

## Mods aren't showing

There are several reasons we've come across so far.

### Forgot to install Forge

For a more detailed version, refer to Step 4 in [Microcontroller's guide](https://microcontrollersdev.github.io/Alternatives/launcher/prism\_win/#step-4-creating-an-instance)

* Open `Instance Settings` by right-clicking the instance and pressing `Edit`
* Take a screenshot of the `Versions` tab and upload it to your ticket, if applicable
* If Forge is not there, press the `Install Forge` button and download the latest version
  * **Latest version:** `11.15.1.2318`

### Incorrectly moved mods to the mods folder

For a more detailed version, refer to Step 5 in [Microcontroller's guide](https://microcontrollersdev.github.io/Alternatives/launcher/prism\_win/#step-5-installing-our-mods-skyclient)

* Open `Instance Settings` by right-clicking the instance and pressing `Edit`
* Take a screenshot of the `Mods` tab and upload it to your ticket, if applicable
* If mods aren't showing, and either **empty** or only show **folders**, the mods were incorrectly installed
  * For Windows users, we highly recommend watching this [video guide](https://www.youtube.com/watch?v=DEGaD-\_HFCE)

