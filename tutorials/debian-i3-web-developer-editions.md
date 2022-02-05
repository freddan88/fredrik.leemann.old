## Debian Linux XFCE + i3 Web Developer Edition

> Tutorial to install Debian with either XFCE-desktop + i3-wm or LXDE-packages + i3-wm

[License: MIT](https://choosealicense.com/licenses/mit)

| My Links: |                                                                                      |
| --------- | ------------------------------------------------------------------------------------ |
| WebPage:  | [leemann.se/fredrik](http://www.leemann.se/fredrik)                                  |
| LinkedIn: | [linkedin.com/fredrik-leemann](https://se.linkedin.com/in/fredrik-leemann-821b19110) |
| GitHub:   | [github.com/freddan88](https://github.com/freddan88)                                 |

Tutorials are tested for:

-   Debian Linux 11 (bullseye) 64Bit

### Installation

##### First download and install Debian Linux from any of the links below:

-   [Download Debian Linux ISO (netinst)](https://www.debian.org/download)
-   [Download Debian Linux ISO (nonfree)](https://cdimage.debian.org/cdimage/unofficial/non-free/cd-including-firmware)

#### 1. Update system and install packages and add your user as sudo-user (run as root) OBS: Will reboot your computer!

```bash
su -
```

```bash
apt update && apt install wget sudo -y && usermod -aG sudo <YOUR_USER_NAME> && apt upgrade -y && reboot
```

### OPTION_1: Install Debian Linux with XFCE-desktop and i3 window-manager

#### 1-1. Install Debian on your computer with the XFCE-desktop

#### 1-2. Download the installation-script (run as user)

```bash
cd && wget -O debian-i3_x64.sh https://raw.githubusercontent.com/freddan88/fredrik.linux.files/main/i3/debian-i3-xfce_x64.sh
```

#### 1-3 Set environment-variable for URL on where to download i3-config file (run as user)

```bash
export URL_I3_CONFIG="https://raw.githubusercontent.com/freddan88/fredrik.linux.files/main/i3/configs/config-i3-xfce.txt"
```

### OPTION_2: Install Debian Linux with LXDE-panel and i3 window-manager

#### 1-1. Install Debian on your computer with no desktop

#### 1-2. Download the installation-script (run as user)

```bash
cd && wget -O debian-i3_x64.sh https://raw.githubusercontent.com/freddan88/fredrik.linux.files/main/i3/debian-i3-lxde_x64.sh
```

#### 1-3 Set environment-variable for URL on where to download i3-config file (run as user)

```bash
export URL_I3_CONFIG="https://raw.githubusercontent.com/freddan88/fredrik.linux.files/main/i3/configs/config-i3-lxde.txt"
```

#### 2. Execute the installation-script as sudo (run as user)

```bash
cd && chmod 754 debian-i3_x64.sh && sudo ./debian-i3_x64.sh install
```

#### 3. Download the main-installation script and execute it (run as user)

```bash
cd && wget https://raw.githubusercontent.com/freddan88/fredrik.linux.files/main/i3/debian-i3-main_x64.sh
```

```bash
cd && chmod 754 debian-i3-main_x64.sh && sudo ./debian-i3-main_x64.sh install
```

#### 4. Download and install tools (run as user)

##### Oh My Zsh: https://ohmyz.sh

```bash
cd && sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
```

##### Zsh extension: autosuggestions: https://github.com/zsh-users/zsh-autosuggestions

```bash
cd && git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

##### Node & npm version control: https://github.com/nvm-sh/nvm

```bash
cd && wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
```

#### 5. Download and update your zsh-config (run as user)

```bash
cd && sudo ./debian-i3-main_x64.sh zsh-config
```

#### 6. Cleanup system and update packages (run as user) OBS: Will reboot your computer!

```bash
cd && rm -f debian-i3_x64.sh && sudo apt update && sudo apt upgrade -y && sudo apt autoremove -y && sudo reboot
```

#### 7. Command to run after reboot (run as user)

```bash
nvm install --lts && nvm alias default node && nvm use node
```

#### VM:S using virtualbox will have to install those to be able to install: VIRTUALBOX GUEST EXTENSIONS

```bash
sudo apt install linux-headers-$(uname -r) make gcc dkms build-essential -y
```

#### Links

-   https://github.com/freddan88/debian-linux-i3-develolper/blob/master/debian_install_i3-2.txt
-   https://github.com/denesb/xfce4-i3-workspaces-plugin
-   https://github.com/freddan88/xubuntu-i3wm
