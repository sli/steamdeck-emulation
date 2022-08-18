# bsnes Guide

❗ Follow the [Getting Started section](../README.md#getting-started) of `README.md` first.

This section of the guide explains how to setup [bsnes](https://github.com/bsnes-emu/bsnes), a Super NES/Super Famicom emulator.

## Installing bsnes

Open Discover, SteamOS' app store, then search for **bsnes**, then click on it.

In the top right, then press **Install**.

Alternatively, open up a terminal and run

```bash
flatpak install --user -y dev.bsnes.bsnes
```

## Configuring bsnes

Open up the emulator, then navigate to **Settings > Input**. Map the controller inputs as desired.

Switch to the Hotkeys tab on the left to bind any desired hotkeys. Note: bsnes does not support the grip buttons.

## Steam ROM Manager

Open Steam ROM Manager, press Parsers, then enter the following settings:

-   Select `Nintendo SNES - Retroarch(Flatpak) - Beetle bsnes` under Community Presets.
    -   Steam ROM Manager doesn't have a preset for non-RetroArch bsnes, so we're going to modify the RetroArch one.
-   You can add additional categories to Steam category using the format `${category name}`, this is case-sensitive.
-   Change configuration title to `Nintendo SNES - bsnes` to make it less confusing.
-   Set executable to `/usr/bin/flatpak`.
-   Set command line arguments to `run dev.bsnes.bsnes --fullscreen "${filePath}"`
-   Set ROMs directory to wherever your SNES ROMs are - if you're using the recommended path, this should be `~/roms/snes`.
-   Press save.

Go to the Preview tab, then press Generate App List. You should see your games populated. You can change the cover art used by hovering over the game and pressing the arrows.

If it looks fine, press Save app list. Load up Steam or switch out of desktop mode, then check your library - you should see your SNES games!