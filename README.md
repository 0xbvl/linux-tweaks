# apt install (my setup)
```
sudo apt-get install
```

- neofetch - command-line system information tool
- synaptic - lightweight GUI front end to apt package management system
- firefox
- vlc
- gdebi - .deb packages
- thunar - modern file manager for the Xfce Desktop Environment
- pcmanfm - file manager application and the standard file manager of LXDE
- gufw - graphical utility for managing Uncomplicated Firewall (UFW)
- nextdns - firewall for the modern Internet /blocker
- stacer - open source system optimizer and application monitor
- htop - interactive real-time process monitoring application
- gedit - text editor designed for the GNOME desktop environment


# speed up grub
```
gedit admin:///etc/default/grub
GRUB_TIMEOUT=1
sudo -s
update-grub
```

# change swapiness value
```
gedit admin:///etc/sysctl.conf
vm.swappiness=10
reboot
```

# incrase zswap value
```
gedit admin:///etc/default/grub
GRUB_CMDLINE_LINUX_DEFAULT="quiet splash zswap.enabled=1 zswap.max_pool_percent=40"
GRUB_CMDLINE_LINUX="zswap.max_pool_percent=40"
sudo update-grub
reboot
```

# check current swapiness value
```
cat /proc/sys/vm/swappiness
check zswap value
cat /sys/module/zswap/parameters/max_pool_percent
```
