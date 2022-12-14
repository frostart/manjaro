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
sudo pacman -S mc htop neofetch gh code inxi ripgrep gdu ranger nnn alacritty --noconfirm
```
Добавляем репозиторий AUR
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

