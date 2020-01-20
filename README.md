# RPCS3 Setup to Retropie

This will add an entry on Retropie-Setup for RPCS3 emulator.

## Install

If PS3 is not added to platforms config file, edit `~/RetroPie-Setup/platforms.cfg` and add:

```
ps3_exts=".ps3"
ps3_fullname="PlayStation 3"
```

After that, install the script with:

```bash
wget https://github.com/raelgc/retropie_rpcs3/blob/master/rpcs3.sh -O ~/RetroPie-Setup/scriptmodules/emulators/rpcs3.sh
```

Now you can run RetroPie Setup and `rpcs3` will available under `Experimental` packages section.

After dump your original PS3 game, move your .PS3 game folders to `ps3` roms folder.
