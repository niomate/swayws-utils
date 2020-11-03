# i3-new-workspace
Automatic workspace creation script for i3 tiling window manager (http://i3wm.org/), adapted for `swaywm`.

Suggested usage: 

Download the repo, and create a symlink in `$HOME/.local/bin`:

    ln -s /path/to/the/repo $HOME/.local/bin/i3-new-workspace

You can then use it from your sway config by adding this line to `$HOME/.config/sway/config`:

    bindsym $mod+n exec i3-new-workspace    # Or whatever keybind you want to use
    
    
# Future plans:
Try to extract whether i3 or sway is used and adjust accordingly.
