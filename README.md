Dump Debian distro installed packages:

dpkg -l | grep ^ii | awk '{print $2}' > debian-installed


Install from dumped file.

sudo apt-get install $(cat debian-installed)


Dump MacOS - brew package manager

brew list > macos-installed

Reinstall in Terminal using brew:

xargs brew install < macos-installed
