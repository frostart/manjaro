# Установка Manjaro Linux

## Исправление ошибок
### 1. Error connecting to Touchégg daemon: Could not connect: Connection refused

```
systemctl disable --now touchegg
```
```
pacman -Rcsu touchegg
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

## Git
```
gh auth login
```

