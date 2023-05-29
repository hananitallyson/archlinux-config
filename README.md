# Development Enviroment Setup on Arch Linux

This README helps me with my Archlinux configuration!

<br>

## Softwares, Repositories and Packages
- [Valet Linux](https://github.com/cpriego/valet-linux-docs)
- [Docker Engine](https://wiki.archlinux.org/title/docker)

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
Some PHP extensions:
```sh
sudo apt install php-mbstring php-cli php-curl php-xml php-zip php-mysql php-pgsql php-sqlite3
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
