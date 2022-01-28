## Debian Linux XFCE + i3 Web Developer Edition Version 01

> Tutorial on how to install Debian Linux with XFCE and i3 window manager + Tools for web-developing

[Tutorial License: MIT](https://choosealicense.com/licenses/mit/)

| My Links: |                                                                                      |
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

> Login as root

```bash
su -
```

#### 1. Update your package manager and system (run as root) OBS: Will reboot your computer!

```bash
apt update && apt upgrade -y && reboot
```

#### 2. Download new wallpaper (run as root)

`cd /tmp && mkdir -p /usr/share/wallpaper`<br/>
`wget https://img.wallpapersafari.com/desktop/1920/1080/95/51/LEps6S.jpg && mv LEps6S.jpg /usr/share/wallpaper/linux-wallpaper-01.jpg`

#### 3. Download and install new themes (run as root)

Link: http://packages.linuxmint.com/pool/main/m

`cd /tmp && wget http://packages.linuxmint.com/pool/main/m/mint-x-icons/mint-x-icons_1.6.4_all.deb`<br/>
`cd /tmp && wget http://packages.linuxmint.com/pool/main/m/mint-y-icons/mint-y-icons_1.5.9_all.deb`<br/>
`cd /tmp && wget http://packages.linuxmint.com/pool/main/m/mint-y-theme/mint-y-theme_1.2.3_all.deb`

```bash
apt install ./mint-y-icons_*_all.deb ./mint-x-icons_*_all.deb ./mint-y-theme_*_all.deb -y
```

#### 4. Download and install software (run as root)

```bash
apt update && apt install i3 zsh git zip wget curl nano sudo net-tools gparted synaptic neofetch nitrogen imagemagick xfce4-screenshooter xfce4-appmenu-plugin compton gimp lightdm slick-greeter && apt autoremove -y
```

Docker: https://docs.docker.com/engine/install/debian

`apt install ca-certificates curl gnupg lsb-release`<br/>
`curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg`<br/>
`echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/debian $(lsb_release -cs) stable" tee /etc/apt/sources.list.d/docker.list > /dev/null`

```bash
apt install docker-ce docker-ce-cli containerd.io -y
```

Add your user to sudo-group

`usermod -aG sudo <your-username>`

Add your user to docker-group

`usermod -aG docker <your-username>`

#### 5. Add configuration for login manager

> echo [Greeter] > /etc/lightdm/slick-greeter.conf<br/>
> echo background=/usr/share/wallpapers/linux-wallpaper-01.jpg >> /etc/lightdm/slick-greeter.conf<br/>
> echo draw-user-backgrounds=false >> /etc/lightdm/slick-greeter.conf<br/>
> echo theme-name=Mint-Y-Dark >> /etc/lightdm/slick-greeter.conf<br/>
> echo icon-theme-name=Mint-Y-Dark >> /etc/lightdm/slick-greeter.conf<br/>
> echo activate-numlock=true >> /etc/lightdm/slick-greeter.conf<br/>
> echo draw-grid=false >> /etc/lightdm/slick-greeter.conf<br/>

#### 6. Download and install tools (run as user)

Oh My Zsh: https://ohmyz.sh

`sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"`<br/>
`git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions`

Node & npm version control: https://github.com/nvm-sh/nvm

```bash
cd /tmp && wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
```

`nvm install --lts`

https://github.com/freddan88/debian-linux-i3-develolper/blob/master/debian_install_i3-2.txt

https://github.com/denesb/xfce4-i3-workspaces-plugin

https://github.com/freddan88/xubuntu-i3wm

FOR VM:S (VIRTUALBOX GUEST EXTENSIONS)
apt install linux-headers-$(uname -r) make gcc dkms build-essential -y
