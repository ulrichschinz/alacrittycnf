# My alacritty cnf

## What is it for?
To have one conifg with tmux started, which I use constantly.  
But I'd like to avoid to have tmux started, if I want to ssh to machines with tmux running on the remote system.  

## How I use it

I'm using i3 windowmanager. There I have defined 2 shortcuts to start alacritty:  
* with standard config (alacritty.yml - `tmux attach || tmux` on startup of alacritty)
* wot config (alacritty-wot.yml - wot means **W**ith**O**ut**T**mux)
  
```bash
) grep alacr .config/i3/config
bindsym $mod+Return exec alacritty
bindsym $mod+Shift+Return exec alacritty --config-file ~/.config/alacritty/alacritty-wot.yml
exec --no-startup-id i3-msg 'workspace 1; exec /usr/bin/alacritty'
```
