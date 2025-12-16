# Active's Bin
A collection of short and useful Arch-/Linux-related scripts. Most are written in Bash.

Most are written by me but few are taken from online sources. In those cases, attribution is given in-script.

# CLI Options
Currently, they all accept Unix-style short options (E,g, `-a`) **and** GNU-style long options (E.g. `--all`).
For options that take an argument, it may either written directly, seperated by a space, or seperated by an equals sign.
I recommend always using an equals, however that is simply a matter of style.

I do my best to follow the best-practices recommended by [The Art of Unix Programming](http://catb.org/~esr/writings/taoup/html/index.html) in his segment about [CLI options](http://catb.org/~esr/writings/taoup/html/ch10s05.html).
**IMPORTANT**: Chaining of Unix-style short options is currently not supported!

A few examples:
```bash
create-script foo

# The below 2 are identical.
create-script foo -b -e
create-script foo --blank --editor

# The below 3 are identical.
create-script -b foo
create-script foo -b
create-script foo --blank
```

However, the following is currently not implemented.
```bash
create-script foo -bn    # ERROR: NOT valid!
```

# Notable Scripts
All scripts have `-h/--help` options which describe their usage. However here is a summary of some of my favourites.

- create-script
    - Creates a new script(s), in your directory of choice. Sets it to be executable by the current user. And fills it with a nice template. Then opens it using your $EDITOR.
- get-x11-window-owner
    - Gets the executable responsible for a particular window. Allows selecting your target window with the mouse.
- sum-video-durations
    - Goes through a given directory (optionally; recursively) and sums the durations of all videos found within.
- popup-new-file-dialog
    - Brings up a yad dialog with powerful options for creating blank files.
- popup-date-time-notification
    - Shows a notification with the current date, time, year-week, and unix-time. Useful if you don't like taskbars. :P

# TODO List
General (mostly `create-script`'s template):
[x] Implement basic option handling.
- [x] Update most scripts with safety features and better exit codes.
- [ ] Implement parsing of chained of Unix-style short options.
- [ ] Implement better parsing of options with arguments.
- [ ] Implement forced positional arguments.
- [ ] Implement support for man pages.

# Credit
Dulfiqar 'Active Diamond' H. Al-Safi

# License
MIT
