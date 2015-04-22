
 ____   ___  _   ___   __  _     ___   ____ 
|  _ \ / _ \| \ | \ \ / / | |   / _ \ / ___|
| |_) | | | |  \| |\ V /  | |  | | | | |  _ 
|  __/| |_| | |\  | | |   | |__| |_| | |_| |
|_|    \___/|_| \_| |_|   |_____\___/ \____|


# SSH LOG
* if you would like to have a nive pony
welcoming you when you start a ssh session
on your server :

### install figlet to enable ASCII art
>sudo apt-get install figlet

### create directory
$> sudo mkdir /etc/update-motd.d

$> sudo emacs /etc/update-motd.d/00-ponies

$> sudo cat /etc/update-motd.d/00-ponies
#! /bin/sh
echo "==============================================="

echo "Welcome $USER" | figlet | ponysay

### make files executable
$> chmod +x /etc/update-motd.d/*

### remove MOTD file
$> rm /etc/motd

### symlink dynamic MOTD file
$> ln -s /var/run/motd /etc/motd


### BASHRC LOG
* else if you would like to have a nive pony
welcoming you when you source your session bash :

### add the script on your bashrc
$> cat >> ~/.bashrc << EOF
echo "Welcome $USER" | figlet | ponysay
EOF

### just check
$> source ~/.bashrc
