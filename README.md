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
### 1. Midnight Commander
```
sudo pacman -S mc
```
### 2. Htop
```
sudo pacman -S htop
```
### 2. Neofetch
```
sudo pacman -S neofetch
```
### 3. Gh
```
sudo pacman -S gh
```
### 4. Code
```
sudo pacman -S code
```

