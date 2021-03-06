# Wall-d
A simple and fast wallpaper manager for x

Features:
- It supports single (same wall on all available screens), dual and triple (different walls on each monitor)
- Uses dmenu for selecting Mode (single, dual or triple) and options (Zoom, Tile, Center, Stretch and no-randr).
- Uses sxiv to preview the wallpapers in thumbnail mode.
- uses xwallpaper to set the wallpaper.
- sxiv window centers in the screen when in floating mode, and respects *.forgorund *.background and *.font settings from .Xresources.
- pywal support

Installation:

Install the depencencies:

- sxiv
- dmenu
- xwallpaper
- pywal (optional)

Clone the repository
```shell
git clone https://github.com/ronniedroid/Wall-d.git
```
then cd into Wall-d then run install.sh
```shell
cd Wall-d
./install.sh
```
or just copy Wall-d and defaultwallpaper.sh to your `$HOME/.local/bin/` directory and make sure that it is in your PATH.

Usage:

-h print this help message and exit

-d path/to/your/wallpapers/directory

-r restore last set Wallpaper(s)

-p Change colorscheme using pywal (Put wal -R in your autostart script to restore last set colorscheme)

to use Wall-d you must define a wallpapers directory useing the `-d` flag.

- Select a mode from dmenu and sxiv will open in thumbnail mode. (in case you have only one monitor connected, you will not be prompt to select a mode and sxiv will open directly in single mode)
- mark the wallpaper you want to set with with m, then press q to quit sxiv. (In single mode, the last marked wallpaper will be used. In dual mode, the last two marked wallpapers will be used. The before-last will be set on Monitor1 and the last will be set on Monitor2 and same with triple mode)
- select am option from dmenu. (you'll have to select an option for each monitor in dual and triple mode)

to restore your last set wallpaper(s) use the `-r` falg. put `Wall-d -r` in your autostart script

sxiv usage:

- hjkl to navigate.
- Return: toggle between thumbnail and image mode.
- m: to mark an picture in thumbnail mode.
- b: show details bar about current picture.
- f: toggle fullscreen mode.

If anyone has suggestions or can contribute to make the script even better, you are welcome to give your feedback or send a pole request.
