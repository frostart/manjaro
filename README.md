# Установка Manjaro Linux

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
### 2. Установка пакетов
```
sudo pacman -S mc htop neofetch gh
```
