ubuntu-misc
===========

blueman

sudo visudo

sudo grub-editenv - unset recordfail

sudo gedit /etc/rc.local

```
tlp start

exit 0
```


terminator 
xbacklight
wmctrl
fcitx-mozc


 xbacklight -set 10
 
 
wmctrl -xa terminator.Terminator || terminator





Download the .deb packages.

$ wget http://kernel.ubuntu.com/~kernel-ppa/mainline/v4.0-rc3-vivid/linux-headers-4.0.0-040000rc3_4.0.0-040000rc3.201503082035_all.deb

$ wget http://kernel.ubuntu.com/~kernel-ppa/mainline/v4.0-rc3-vivid/linux-headers-4.0.0-040000rc3-generic_4.0.0-040000rc3.201503082035_amd64.deb

$ wget http://kernel.ubuntu.com/~kernel-ppa/mainline/v4.0-rc3-vivid/linux-image-4.0.0-040000rc3-generic_4.0.0-040000rc3.201503082035_amd64.deb
Install them.

$ sudo dpkg -i linux-headers-4.0*.deb linux-image-4.0*.deb
Reboot the system.

sudo reboot

To uninstall,

sudo apt-get remove 'linux-headers-4.0*' 'linux-image-4.0*'

