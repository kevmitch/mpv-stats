mpv-stats
---------
Display statistics for the currently played file in mpv.

![Default](https://cloud.githubusercontent.com/assets/540920/8833849/3249999a-30b1-11e5-9e63-53aaf777d9ea.jpg)

Usage
-----
Place `stats.lua` in your `~/.config/mpv/scripts/` or `~/.mpv/scripts/` folder
to autoload the script. Alternatively load it with `--script=<path>`.

The script is binding itself to `i` (however, not overriding your own bindings)
and can therefore be invoked with this key.
You can create different bindings by adding `<yourkey> script_binding stats` to
`input.conf`.

Customization
-------------
You can configure some settings by creating a file `stats.conf` in a folder
named `lua-settings` within your mpv folder.
Please refer to the `o` table within the script for possible option names and
consult [mpv manual](http://mpv.io/manual/master/#config-syntax) regarding
configuration syntax.

To change e.g. the text display duration your `stats.conf` may look like:

    duration=5

A more sophisticated example:

    font=Arial
    font_size=9
    font_color=262626
    border_size=0.5
    border_color=FFFFFF
    alpha=70
    duration=5
    debug=yes

Note: colors are given as hexadecimal values and use
[ASS tag](http://docs.aegisub.org/3.2/ASS_Tags/#\c) order: BBGGRR (blue green red).
