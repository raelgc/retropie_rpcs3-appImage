# RPCS3 Setup for Retropie

This will add an entry on [Retropie-Setup](https://github.com/RetroPie/RetroPie-Setup) for [RPCS3 emulator](https://rpcs3.net) running on a X86 (aka PC) machine.

## Requirements

Check if you have PS3 already listed in file `~/RetroPie-Setup/platforms.cfg`.

If not, create (or edit) file `/opt/retropie/configs/all/platforms.cfg` and add:

```
ps3_exts=".ps3"
ps3_fullname="PlayStation 3"
```

## Install

After that, install the RPCS3 setup script with:

```bash
wget https://raw.githubusercontent.com/raelgc/retropie_rpcs3-appImage/master/rpcs3-appImage.sh -O ~/RetroPie-Setup/scriptmodules/emulators/rpcs3-appImage.sh
```

Now you can run **RetroPie Setup** script and `rpcs3` will available under `exp` (experimental) packages section.

## Games folder

After dump your original PS3 game, move the game content to a folder with a `.PS3` extension under `~/RetroPie/roms/ps3/`.

Example: if your game is `Skate3`, put content under `~/RetroPie/roms/ps3/Skate3.PS3/`

## PSN game

PSN games uses `.pkg` extension.

### Install

Open RPCS3: from a terminal, run `/opt/retropie/emulators/rpcs3/bin/rpcs3.AppImage`.

Then, into RPCS3 menu, select `File` > `Install .pkg`.

Browse and select the `.pkg` content to run.

### EmulationStation

In order to create an entry for the PSN game, take note of the game **serial** (you can copy the game serial on RPCS3 UI, right clicking in the game and select "Copy info" > "Copy game serial").

Then create a folder for your game  with a `.PS3` extension under `~/RetroPie/roms/ps3/` (remember to replace the **game name** by your actual game name):

    mkdir ~/RetroPie/roms/ps3/<replace-with-your-game-name>.PS3

Create a shortcut from the PS3 internal storage to the `~/RetroPie/roms/ps3/` (remember to replace the **serial** and **game name** by your actual game values):

    ln -sf  ~/.config/rpcs3/dev_hdd0/game/<serial> ~/RetroPie/roms/ps3/<replace-with-your-game-name>.PS3/PS3_GAME

## Playing

Check [RPCS3 Quick Start guide](https://rpcs3.net/quickstart).
