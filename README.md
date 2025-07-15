Dump Debian distro installed packages:

dpkg -l | grep ^ii | awk '{print $2}' > debian-installed


Install from dumped file.

sudo apt-get install $(cat debian-installed)


Dump MacOS - brew package manager

brew list > macos-installed

Reinstall in Terminal using brew:

xargs brew install < macos-installed


Dump Arch linux packages

yay -Qqe > arch-linux-installed

Reinstall  packages:
yay -S (cat arch-linux-installed)
or
yay -S --needed - < arch-linux-installed

