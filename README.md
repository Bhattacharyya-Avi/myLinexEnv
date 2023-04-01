# The solution of problem i have faced and what software i am using on my setup

## Install the things on root or home directory. Use the command to see the current path

```bash
pdw
``` 

## If have issue with network driver follow the commands. <a href = "https://www.technolaty.com/how-to-install-wireless-drivers-on-ubuntu/">Source</a>. 

```bash
sudo apt install network-manager
``` 
```bash
sudo apt update && sudo apt upgrade
``` 
```bash
sudo lshw -C network
``` 

## Let's start with Ubuntu environment setup
## CURL
```bash
sudo apt install curl
``` 
```bash
curl --version
``` 

### Note: If you want to use apache please follow  <a href = "https://httpd.apache.org/">official website </a>. I am using ngnix.
## NGNIX
```bash
sudo add-apt-repository ppa:ondrej/php
``` 
```bash
sudo apt install -y php-mbstring php-xml php-fpm php-zip php-common php-fpm php-cli unzip
curl nginx
``` 
```bash
apt-get install nginx
``` 
```bash
sudo apt install software-properties-common
``` 

## PHP
### Note: please change php version if you don't want to use php8.0 Get info about php version on <a href = "https://www.php.net/releases/index.php">php release notes</a>.
```bash
sudo apt install php8.0-fpm
``` 
```bash
php -v
``` 
```bash
sudo apt-get install php8.0-mysql php8.0-mbstring php8.0-xml php8.0-bcmath
``` 
```bash
systemctl status php8.0-fpm
``` 

## Composer
```bash
sudo curl -s https://getcomposer.org/installer | php
``` 
```bash
sudo mv composer.phar /usr/local/bin/composer
``` 
```bash
sudo curl -s https://getcomposer.org/installer | php
``` 
### For check composer is installed or not run command on terminal
```bash
composer
``` 

## Laravel install
```bash
sudo composer global require laravel/installer
```
### Create Laravel project
```bash
composer create-project laravel/laravel example-app/laravel project name
```

## Mysql:
```bash
 sudo apt upgrade && sudo apt update
```
```bash
sudo apt install mysql-client
```
```bash
sudo apt install mysql-server
```
```bash
sudo mysql_secure_installation
```
```bash
mysql --version
```
### go to mysql panel
```bash
sudo mysql
```
or
```bash
mysql -u root -p
```
### Change mysql password 
```bash
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password by 'your database password';
```
### Create New Database and show list of databases
```bash
mysql -u root -p
```
Note: replace databasename with your Database name
```bash
create database databasename;
```
```bash
show databases;
```

## Tableplus [For more info goto <a href="https://tableplus.com/blog/2019/10/tableplus-linux-installation.html"> Tableplus official site </a>]
### Note: Works untill ubuntu 20 LTS version
```bash
wget -qO - https://deb.tableplus.com/apt.tableplus.com.gpg.key | sudo apt-key add -
```
```bash
sudo add-apt-repository "deb [arch=amd64] https://deb.tableplus.com/debian/20 tableplus main"
```
```bash
sudo apt update
```
```bash
sudo apt install tableplus
```
### For Ubuntu 22 LTS version
```bash
wget -qO - https://deb.tableplus.com/apt.tableplus.com.gpg.key | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/tableplus-archive.gpg > /dev/null
```
```bash
sudo add-apt-repository "deb [arch=amd64] https://deb.tableplus.com/debian/22 tableplus main"
```
```bash
sudo apt update
```
```bash
sudo apt install tableplus
```

## Git

```bash
sudo apt-get update
```
```bash
sudo apt-get install git
```
```bash
git config --global user.name "your github username"
```
```bash
git config --global user.email "your github attached email address"
```
```bash
ssh-keygen -t rsa -b 4096 -C "your github attached email address"
```
```bash
eval "$(ssh-agent -s)"
```
```bash
ssh-add -K /Users/you/.ssh/id_rsa
```

## Vs code

```bash
sudo apt-get install wget gpg
```
```bash
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
```
```bash
sudo install -o root -g root -m 644 packages.microsoft.gpg /etc/apt/trusted.gpg.d/
```
```bash
sudo sh -c 'echo "deb [arch=amd64,arm64,armhf signed-by=/etc/apt/trusted.gpg.d/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" > /etc/apt/sources.list.d/vscode.list'
```
```bash
rm -f packages.microsoft.gpg
```
### Then update the package cache and install the package using:

```bash
sudo apt update
```
```bash
sudo apt install apt-transport-https
```
```bash
sudo apt update
```
```bash
sudo apt install code
```

## wget install if it give an error 

```bash
sudo apt install wget
```

## Google Chrome install

```bash
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
```
```bash
sudo apt install ./google-chrome-stable_current_amd64.deb
```

# End of the main part of setup env in ubuntu
☕ ❤️☕ ❤️☕ ❤️☕ ❤️☕ ❤️☕ ❤️☕ ❤️☕ ❤️☕ ❤️☕ ❤️☕ ❤️☕ ❤️☕ ❤️☕ ❤️☕ ❤️☕ ❤️☕ ❤️☕ ❤️☕ ❤️☕ ❤️

# Additional things

## valet install 
```bash
composer global require cpriego/valet-linux
```
```bash
sudo apt-get install php-curl
```
```bash
test -d /.composer && bash /.config/composer/vendor/bin/valet install
```
```bash
(export PATH=$PATH:~/.config/composer/vendor/bin
ls -al ~/.config/composer/vendor/bin/valet
source ~/.bash_profile)
```
```bash
valet install
```
To check valet is installed or not
```bash
valet
```
To add directory to valet
```bash
valet park
```

If when package is unable to locate
```bash
(test -d /.composer && bash /.composer/vendor/bin/valet install || bash~/.config/composer/vendor/bin/valet install)
```

## For customize the default ubuntu terminal with zsh and modify little bit followed this <a href="https://www.youtube.com/watch?v=PZTLIVQxxEY&t=667s&ab_channel=MuhammadbinYusrat">video</a> 
### Note : You can go with your loved vedio. 🙂

## Give file edit or modify related permission
### Note: please run the command if you get issue related with that
```bash
sudo chmod 777 -R /var/www/html
```

## Migration driver not found error during migrate command
### Note: please run the command if you get issue related with that
```
sudo apt-get install php-mysql
```

## Package releted issue due to Composer installation or update on project
```
composer install --ignore-platform-reqs
```

## Remove application from ubuntu
```
sudo apt-get remove package-name
```

## Hide mounted drive form the dock
```
gsettings set org.gnome.shell.extensions.dash-to-dock show-mounts false
```

## re-enable mounted drives on the Ubuntu Dock in future
```
gsettings set org.gnome.shell.extensions.dash-to-dock show-mounts true
```

# Author Avindra bhattacharyya
### <a href="mailto:ab.cse.dev@gmail.com">📧</a>
### Thankyou 🌻