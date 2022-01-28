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

#### 1 Update your package manager lists and system (run as root):

```bash
apt update && apt upgrade -y
```

---

Reboot your computer

---

#### 2 Download and install software (run as root):

```bash
apt install i3 zsh git ssh zip wget curl nano sudo net-tools slick-greeter gparted synaptic neofetch nitrogen imagemagick mirage xfce4-screenshooter compton gimp lightdm -y
```

- https://github.com/freddan88/debian-linux-i3-develolper/blob/master/debian_install_i3-2.txt
