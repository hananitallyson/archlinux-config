# Development Enviroment Setup on Arch Linux

This README helps me with my Archlinux configuration!

<br>

## Softwares, Repositories and Packages
- [ArchLinux AUR](https://aur.archlinux.org/)
- [ArchLinux Official](https://archlinux.org/packages/)
- [Laravel Valet on Linux](https://cpriego.github.io/valet-linux/)
- [Laravel Takeout](https://github.com/tighten/takeout)
- [Zinit](https://github.com/zdharma-continuum/zinit)
- [Docker Engine](https://wiki.archlinux.org/title/docker)
- [Yay](https://aur.archlinux.org/packages/yay)
- [Beekeeper](https://aur.archlinux.org/packages/beekeeper-studio-bin)
- [Flatpak](https://flatpak.org/setup/)

<br>

## Installation Commands

**Installing Git**

```sh
sudo pacman -S git
```

<br>

**Installing Curl**

```sh
sudo pacman -S curl
```

<br>

**Installing PHP**

```sh
sudo pacman -S php
```

<br>

**Installing Composer**
[Composer](https://getcomposer.org/download/)
Most likely, you want to put the composer.phar into a directory on your PATH, so you can simply call composer from any directory (Global install), using for example:
```sh
sudo mv composer.phar /usr/local/bin/composer
```
.bashrc or .zshrc:
```
export PATH=$PATH:$HOME/.config/composer/vendor/bin/
```

<br>

**Installing Laravel**

```sh
composer global require laravel/installer
```

<br>

**Installing Node**

First of all, install NVM (Node Version Manager):
```sh
curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash
```
Then execute the command below:
```sh
source ~/.bashrc
```
Or _~/.zshrc_ if you use zshell.

Then, install Node:
```sh
nvm install node
```
<br>

**Installing Python & PIP**

```sh
sudo pacman -S python
```

```sh
sudo pacman -S python-pip
```

<br>

**Installing ZSH**

```sh
sudo pacman -S zsh
```

<br>

<hr>

**Commands to not be needed SUDO to run Docker:**
```sh
sudo groupadd docker
sudo usermod -aG docker $USER
```
Then, restart to change it.
