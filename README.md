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

After installing `yay` run `yay -S - < dependencies.txt`. This will install all required dependencies and apps for the custom desktop environment.

Install `oh-my-zsh` with the below command.
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

Install `powerlevel10k` theme for `zsh`.
```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

Install `lunarvim` with the below command.
```
LV_BRANCH='release-1.2/neovim-0.8' bash <(curl -s https://raw.githubusercontent.com/lunarvim/lunarvim/fc6873809934917b470bff1b072171879899a36b/utils/installer/install.sh)
```

Navigate to this directory if not already and run `./install`. This will setup all the config and dotfiles.


