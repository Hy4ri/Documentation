# Waydroid

## Installation

1. install the waydroid pkg from the repo.
2. run `waydroid init`, use `-s GAPPS` to get google apps.
3. `sudo systemctl enable --now waydroid-container` to start waydroid on lunch or use `waydroid session start`.
4. to use waydroid `waydroid show-full-ui`
--
## Enable network

`sudo ufw allow 67`

`sudo ufw allow 53`

`sudo ufw default allow FORWARD`
---
## Tips 

1. change the resloution of the window 

    `waydroid prop set persist.waydroid.width auto`
    `waydroid prop set persist.waydroid.height auto`

* use auto or pixel size like 1920x1080

2. Clean waydroid Installation

    `sudo rm -rf /var/lib/waydroid /home/.waydroid`
    `rm -rf ~/waydroid ~/.share/waydroid ~/.local/share/applications/*aydroid* ~/.local/share/waydroid`

3. To enable arm emulation

    go to this [Script](https://github.com/casualsnek/waydroid_script), use it to enable libhoudini

* can be used to add other features to waydroid 
---
## Google Play Certification

1. Run `sudo waydroid shell`

2. Inside the shell run this command:

    `ANDROID_RUNTIME_ROOT=/apex/com.android.runtime ANDROID_DATA=/data ANDROID_TZDATA_ROOT=/apex/com.android.tzdata ANDROID_I18N_ROOT=/apex/com.android.i18n sqlite3 /data/data/com.google.android.gsf/databases/gservices.db "select * from main where name = \"android_id\";"`

3. Use the string of numbers printed by the command to register the device on your Google Account at [GooglePlay](https://www.google.com/android/uncertified)

4. Give the Google services some minutes to reflect the change, then restart waydroid
