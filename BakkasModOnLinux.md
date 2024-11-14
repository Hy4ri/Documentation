# BakkasMod Linux with heroic lanucher 

## Dependencies

- Heroic games launcher
- Wine
- Winetricks
- ProtonGE

## Steps 
- ProtonGE:
    
    1. Make Sure that you have ProtonGE installed from heroic wine manager and that it used to run rocket League.
    2. Run RocketLeauge once after applying protonGE to make sure the paths are set.

- Paths:

    1. Locate protonGE executable.
        ~/.config/heroic/tools/proton/Proton-GE-Proton[version number]/files/bin/wine

    2. Locate RocketLeauge Prefix.
        ~/[your heroic path]/Prefixes/default/Rocket League/pfx

- Installation of BakkasMod: 

    1. Install BakkasMod From the official website
    2. Extract the file in downloads folder
    3. Run `WINEPREFIX=[your prefix path] [your executable path] ~/Downloads/BakkesModSetup.exe`
    4. Make sure to run all the updates if needed
    5. Disable safe mode from settings

- Injection to the game:

    1. Launch rocket league from heroic
    2. Find what kind of sync your using F or E 
    3. Run `WINE[F/E]SYNC=1 WINEPREFIX=[your prefix path] [your executable path] c:/Program\ Files/BakkesMod/BakkesMod.exe`

- App shortcut to launch BakkasMod:

    1. `nano ~/.local/share/applications/BakkesMod.desktop`
    2. `[Desktop Entry] 
        Name=BakkesMod
        Exec=bash -c 'Script that has the command'
        Type=Application
        Icon=742F_BakkesMod.0`
