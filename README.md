# Manjaro Linux Setup

## Errors repair
### 1. Error connecting to Touchégg daemon: Could not connect: Connection refused

```
sudo systemctl disable --now touchegg
```
```
sudo pacman -Rcsu touchegg
```
```
sudo reboot
```
### 2. Duplicate first key stroke on activities overview

```
gsettings set org.gnome.shell.extensions.dash-to-dock disable-overview-on-startup true
```
### 3. X11 Scaling Factor
```
sudo pacman -S mutter-x11-scaling
```
```
gsettings set org.gnome.mutter experimental-features "['x11-randr-fractional-scaling']"
```
### 4. QT small fonts correction

```
sudo nvim  /etc/profile.d/qt-hidpi.sh  
```
```
export QT_DEVICE_PIXEL_RATIO=1.3
```

## Programms Install
```
sudo pacman -S mc htop neofetch gh code inxi ripgrep gdu ranger nnn alacritty lazygit fzf zoxide npm nodejs tmux docker podman --noconfirm
```
```
sudo pamac install openrgb-bin yandex-browser
```
### Nerd Fonts Setup
```
sudo pamac install nerd-fonts-complete --no-confirm 
```

## Git auth
```
gh auth login
```
### Alacritty Terminal

Copy from ~/git/dotfiles/alacritty.yml to ~/.config/alacritty

Change window.opacity: 0.92 on:
```
window:
  opacity: 0.92
```
Alacri themes install
```
npm i -g alacritty-themes
```
Set alias in ~/.zshrc
```
alias at='alacritty-themes'
```

### Oh My Zsh
```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
### Powerlevel10k
```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```
```
p10k configure
```
### AstroNvim

```
mv ~/.config/nvim ~/.config/nvim.bak
```
```
mv ~/.local/share/nvim ~/.local/share/nvim.bak
mv ~/.local/state/nvim ~/.local/state/nvim.bak
mv ~/.cache/nvim ~/.cache/nvim.bak
```
```
git clone https://github.com/AstroNvim/AstroNvim ~/.config/nvim
nvim
```
### Wireguard

```
sudo pacman -S wireguard-tools
```
```
sudo cp ~/vpn/manjaro-ruvds.conf /etc/wireguard/wg0.conf
```
Поднять
```
wg-quick up wg0 
```
Опустить
```
wg-quick down wg0 
```

