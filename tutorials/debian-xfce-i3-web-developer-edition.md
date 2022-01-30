## Debian Linux XFCE + i3 Web Developer Edition

> Tutorial on how to install Debian Linux with XFCE and i3 window manager + Tools for web-developing

[Tutorial License: MIT](https://choosealicense.com/licenses/mit/)

| My Links: |                                                                                      |
| --------- | ------------------------------------------------------------------------------------ |
| WebPage:  | [leemann.se/fredrik](http://www.leemann.se/fredrik)                                  |
| LinkedIn: | [linkedin.com/fredrik-leemann](https://se.linkedin.com/in/fredrik-leemann-821b19110) |
| GitHub:   | [github.com/freddan88](https://github.com/freddan88)                                 |

This tutorial is tested on:

-   Debian Linux 11 (bullseye) 64Bit

### Installation

> First download and install Debian Linux with XFCE desktop from any of the links below:

-   [Download Debian Linux ISO (netinst)](https://www.debian.org/download)
-   [Download Debian Linux ISO (nonfree)](https://cdimage.debian.org/cdimage/unofficial/non-free/cd-including-firmware)

#### VM:S using virtualbox (VIRTUALBOX GUEST EXTENSIONS)

```bash
apt install linux-headers-$(uname -r) make gcc dkms build-essential -y
```

#### 1. Update system and install some packages (run as root) OBS: Will reboot your computer!

```bash
su -
```

```bash
apt update && apt install wget sudo -y && usermod -aG sudo <YOUR_USER_NAME> && apt upgrade -y && reboot
```

#### 2. Download and execute installation-script as sudo (run as user)

```bash
cd && wget https://raw.githubusercontent.com/freddan88/fredrik.linux.files/main/i3/debian-xfce-i3_x64.sh -O debian-xfce-i3_x64.sh
```

```bash
cd && chmod 754 debian-xfce-i3_x64.sh && sudo ./debian-xfce-i3_x64.sh install
```

#### 3. Download and install tools (run as user)

Oh My Zsh: https://ohmyz.sh

```bash
cd && sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
```

Zsh extension: autosuggestions: https://github.com/zsh-users/zsh-autosuggestions

```bash
cd && git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

Node & npm version control: https://github.com/nvm-sh/nvm

```bash
cd /tmp && wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
```

#### 4. Download and update your zsh-config

```bash
sudo ./debian-xfce-i3_x64.sh zsh-config
```

#### 5. Update packages and cleanup system (run as user) OBS: Will reboot your computer!

```bash
sudo apt update && sudo apt upgrade -y && sudo apt autoremove -y && sudo reboot
```

#### 6. Command to run after reboot

```bash
nvm install --lts
```

#### Links

-   https://github.com/freddan88/debian-linux-i3-develolper/blob/master/debian_install_i3-2.txt
-   https://github.com/denesb/xfce4-i3-workspaces-plugin
-   https://github.com/freddan88/xubuntu-i3wm
