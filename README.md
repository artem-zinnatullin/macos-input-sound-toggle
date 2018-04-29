# macOS Input Sound Toggle

## Motivation

During podcasting or conference calls you might want to quickly toggle input volume on and off.

## Solution

This project provides very simple Bash script that uses `osascript` to get and set system input volume level.

Very important aspect of this implementation is that when it turns input volume back on **it restores volume level to previously saved value**.

## How To Use

1. [Download script](https://raw.githubusercontent.com/artem-zinnatullin/macos-input-sound-toggle/master/toggle-sound-input) or clone the repo.
1. Add executable permissions: `chmod +x ~/Downloads/toggle-sound-input` (not required if you clone repo).
1. Toggle your input sound on or off just by calling it `~/Downloads/toggle-sound-input`!

Ouput example:

```diff
$ ~/Downloads/toggle-sound-input
- Sound input muted.

$ ~/Downloads/toggle-sound-input
+ Sound input level restored to 75.
```

## Tips

### Alias

You can make an alias for the script or add it to `PATH`.

### Assign a Hotkey

You can [assign a hotkey](https://superuser.com/questions/153890/assign-a-shortcut-to-running-a-script-in-os-x/264943) to run the script.

## Credits

Thanks to [Artur Dryomov](https://github.com/ming13) for [tweeting a snippet of `osascript` that was muting the sound](https://twitter.com/arturdryomov/status/989940151165079552), it made me try to script an implementation that'd do it pragmatically.
