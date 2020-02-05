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

After dump your original PS3 game, move the game content to a folder with a `.PS3` extension under `~/Retropie/roms/ps3/`.

Example: if your game is `Skate3`, put content under `~/Retropie/roms/ps3/Skate3.PS3/`

## Playing

Check [RPCS3 Quick Start guide](https://rpcs3.net/quickstart).
