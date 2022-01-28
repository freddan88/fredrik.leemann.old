## Debian Linux XFCE + i3 Web Developer Edition Version 01

> Tutorial on how to install Debian Linux with XFCE and i3 window manager + Tools for web-developing

[Tutorial License: MIT](https://choosealicense.com/licenses/mit/)

| Links:    |                                                                                      |
| --------- | ------------------------------------------------------------------------------------ |
| WebPage:  | [leemann.se/fredrik](http://www.leemann.se/fredrik)                                  |
| LinkedIn: | [linkedin.com/fredrik-leemann](https://se.linkedin.com/in/fredrik-leemann-821b19110) |
| GitHub:   | [github.com/freddan88](https://github.com/freddan88)                                 |

This tutorial is tested on:

- Debian Linux 11 (bullseye) 64Bit

### Installation

> First download and install Debian Linux from any of the links below:

- [Download Debian Linux ISO (netinst)](https://www.debian.org/download)
- [Download Debian Linux ISO (nonfree)](https://cdimage.debian.org/cdimage/unofficial/non-free/cd-including-firmware)

#### 1. Update your package manager and system (run as root) OBS: Will reboot your computer!

```bash
apt update && apt upgrade -y && reboot
```

#### 2. Download new wallpaper (run as root)

```bash
mkdir -p /usr/share/wallpapers && cd /usr/share/wallpapers \
wget https://img.wallpapersafari.com/desktop/1920/1080/95/51/LEps6S.jpg && mv LEps6S.jpg linux-wallpaper-01.jpg
```

#### 3. Download and install new themes (run as root)

```bash

```

#### 4. Download and install software (run as root)

```bash
apt update && apt install i3 zsh git zip wget curl nano sudo net-tools gparted synaptic neofetch nitrogen imagemagick xfce4-screenshooter xfce4-appmenu-plugin compton gimp lightdm slick-greeter -y
```

https://github.com/freddan88/debian-linux-i3-develolper/blob/master/debian_install_i3-2.txt

https://github.com/denesb/xfce4-i3-workspaces-plugin
