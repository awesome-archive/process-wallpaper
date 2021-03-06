# process-wallpaper

Python and shell scripts which set your wallpaper to a wordcloud of the most resource-intensive processes presently running.

![](https://raw.githubusercontent.com/anirudhajith/process-wallpaper/master/screenshot.png)

## Depenendencies
* `python3`
* `gsettings` (comes preinstalled with GNOME) or `feh` (supported by many Linux distributions). 

If neither `gsettings` not `feh` are supported by your platform, you can still set `wallpaper.png` as your wallpaper manually.

## Setup
* Set the resolution of your display in `config.json`
* Use the following commands
```
cd /path/to/script/directory
chmod +x setup.sh
./setup.sh
```

## Use
The wallpaper is updated every time `updateWallpaper.sh` is run. To trigger the update every minute, append the following line to `crontab -e`:
```
* * * * * cd /path/to/script/directory && ./updateWallpaper.sh > /tmp/wallpaper.log 2>&1

```
