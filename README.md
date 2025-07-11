Dump Debian distro installed packages:

dpkg -l | grep ^ii | awk '{print $2}' > debian-installed


Install from dumped file.

sudo apt-get install $(cat debian-installed)
