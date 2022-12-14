# Установка Manjaro Linux

## Исправление ошибок
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
## Установка пакетов
```
sudo pacman -S mc htop neofetch gh code inxi ripgrep gdu ranger nnn alacritty lazygit fzf zoxide npm nodejs tmux docker podman --noconfirm
```
```
sudo pamac install openrgb-bin yandex-browser
```
### Установка шрифтов Nerd
```
sudo pamac install nerd-fonts-complete --no-confirm 
```

## Git
```
gh auth login
```
### Alacritty
Copy from ~/git/dotfiles/alacritty.yml to ~/.config/alacritty

Change window.opacity: 0.92 on:
```
window:
  opacity: 0.92
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

