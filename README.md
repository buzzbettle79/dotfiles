# BuzzBettle DotFiles

Collection of dotfiles for Arch based systems.

Currently holds configs for the following apps.

- Alacritty
- BSPWM
- SXHKD
<!-- - i3 Window Manager -->
- LunarVim and NeoVim (NVChad)
- Newsboat
- Picom
- Ranger
- Rofi
- Zsh, oh-my-zsh, powerlevel10k
- Polybar

## Install

I have attempted to use plugins to do the git cloning and yay installing but they are unmaintained and do not work as intended anymore. Instructions to setup below are for a freshly installed Archlinux environment.

Clone this repo to your machine.

For `./install` to run correctly you need to have already installed both `python` and `git`.
```
sudo pacman -S git base-devel python
```

`yay` must also be installed first

```
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si
```

After installing `yay` run `yay -Syyu && yay -S - < dependencies.txt`. This will install all required dependencies and apps for the custom desktop environment.

Run `chmod +x helper.sh && ./helper.sh`. This will install the following apps `oh-my-zsh powerlevel10k rust lunarvim`.

Navigate to this directory if not already and run `./install`. This will setup all the config and dotfiles.

## Issues

Currently during my testing, following the instructions and then running `startx` gets us into an X11 session successfully, most things work (have not tested extensively) but polybar does not launch and currently in my VM alacritty is unusable even with opacity off (maybe disable picom for VMs?).
