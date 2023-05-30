# Development Enviroment Setup on Arch Linux

This README helps me with my Archlinux configuration!

<br>

## Softwares, Repositories and Packages
- [ArchLinux AUR](https://aur.archlinux.org/)
- [ArchLinux Official](https://archlinux.org/packages/)
- [Docker WSL](https://github.com/codeedu/wsl2-docker-quickstart)
- [Laravel Valet on Linux](https://cpriego.github.io/valet-linux/)
- [Laravel Takeout](https://github.com/tighten/takeout)
- [Zinit](https://github.com/zdharma-continuum/zinit)
- [Docker Engine](https://wiki.archlinux.org/title/docker)
- [Yay](https://aur.archlinux.org/packages/yay)
- [Beekeeper](https://aur.archlinux.org/packages/beekeeper-studio-bin)

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
sudo pacman -S php82
```
Some PHP extensions:
```sh
sudo pacman -Ss php82-mbstring php82-cli php82-curl php82-xml php82-zip php82-mysql php82-pgsql php82-sqlite3
```

<br>

**Installing Composer**

```sh
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === '55ce33d7678c5a611085589f1f3ddf8b3c52d662cd01d4ba75c0ee0459970c2200a51f492d557530c71c15d8dba01eae') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
```
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
