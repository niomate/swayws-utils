# swayws-utils
Originally a fork of `i3-new-workspace`, an automatic workspace creation script for i3 tiling window manager (http://i3wm.org/).
I changed it to work with sway, but also added some more convenience scripts I found useful for my setup.

## Communication

All the scripts use `swayipc.py` to communicate with swaywm. I originally found this module in [this reddit post](https://www.reddit.com/r/swaywm/comments/ey823e/python_module_for_easy_sway_ipc_integration/) and decided it would be a good fit for this project.

## Executables

I created 4 executables for now that I personally found pretty useful in moving around and managing my `swaywm` setup:

- `swaygo <next|prev>`: Similar to the standard workspace next/prev you can use in the sway config. However, this also allows you to got to non-empty workspaces.
- `swaymove <next|prev>`: Similarly to `swaygo`, this command emulates `move container to workspace prev` with the additional feature that you can also move containers to empty workspaces
- `swaygomove <next|prev>`: Combination of both of the above
- `swaynewws`: Creates a new workspace at the lowest possible number

## Suggested usage: 

For now, I haven't written an install script, so you have to do it manually.
Download the repo, and create a symlink in `$HOME/.local/bin` (or any other directory, as long as it is on the `$PATH`):

    ln -s /path/to/the/repo/<name-of-executable> $HOME/.local/bin/

You can then use it from your sway config by adding this line to `$HOME/.config/sway/config`:

    bindsym $mod+n exec --no-startup-id <name-of-executable>    # Or whatever keybind you want to use
    
