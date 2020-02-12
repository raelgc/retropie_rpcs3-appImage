# RPCS3 Setup to Retropie

This will add an entry on [Retropie-Setup](https://github.com/RetroPie/RetroPie-Setup) for [RPCS3 emulator](https://rpcs3.net).

## Install

If PS3 is not added to platforms config file, edit `~/RetroPie-Setup/platforms.cfg` and add:

```
ps3_exts=".ps3"
ps3_fullname="PlayStation 3"
```

After that, install the script with:

```bash
wget https://raw.githubusercontent.com/raelgc/retropie_rpcs3/master/rpcs3.sh -O ~/RetroPie-Setup/scriptmodules/emulators/rpcs3.sh
```

Now you can run **RetroPie Setup** script and `rpcs3` will available under `exp` (experimental) packages section.

## Games folder

### ISO game

After dump your original PS3 game, move the game content to a folder with a `.PS3` extension under `~/RetroPie/roms/ps3/`.

Example: if your game is `Skate3`, put content under `~/RetroPie/roms/ps3/Skate3.PS3/`

### PSN game

#### Install

Open RPCS3: from a terminal, run `/opt/retropie/emulators/rpcs3/bin/rpcs3.AppImage`.

Then, into RPCS3 menu, select `File` > `Install .pkg`.

Browse and select the `.pkg` content to run.

#### EmulationStation

In order to create an entry for the PSN game, take note of the game **serial** (you can see the game serial on RPCS3 UI).

Then create a folder for your game  with a `.PS3` extension under `~/RetroPie/roms/ps3/` (remember to replace the **game name** by your actual game name):

    mkdir ~/RetroPie/roms/ps3/<replace-with-your-game-name>.PS3

Create a shortcut from the PS3 internal storage to the `~/RetroPie/roms/ps3/` (remember to replace the **serial** and **game name** by your actual game values):

    ln -sf  ~/.config/rpcs3/dev_hdd0/game/<serial> ~/RetroPie/roms/ps3/<replace-with-your-game-name>.PS3/PS3_GAME

## Playing

Check [RPCS3 Quick Start guide](https://rpcs3.net/quickstart).
