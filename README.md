ubuntu-misc
===========

blueman

sudo visudo

User alias specification

kenokabe ALL = NOPASSWD: /home/ken/startup

------------
modprobe -r mwifiex_usb
------------

/home/ken/startup <-- executable

shortcut

/etc/bluetooth/main.conf

 commented out AutoConnectTimeout 
 RememberPowered   false.
 
 
 /etc/rc.local

``` 
 # Prevents the Bluetooth USB card from getting reset which disconnects the mouse
BTUSB_DEV="1286:2044"
BTUSB_BINDING="$(lsusb -d "$BTUSB_DEV" |
    cut -f 1 -d : |
    sed -e 's,Bus ,,' -e 's, Device ,/,' |
    xargs -I {} udevadm info -q path -n /dev/bus/usb/{} |
    xargs basename)"


echo "Disabling autosuspend for Bluetooth USB Soundcard: $BTUSB_BINDING..."
echo -1 > "/sys/bus/usb/devices/$BTUSB_BINDING/power/autosuspend_delay_ms"

exit 0
```


 
 
 echo 1 | sudo tee /sys/module/bluetooth/parameters/disable_esco
sudo /etc/init.d/bluetooth restart
# persist setting
echo "options bluetooth disable_esco=1" | sudo tee /etc/modprobe.d/bluetooth-tweaks.conf


HowToSetCapsLockAsCtrl

gnome-tweak-tool

theme

unity-tweak-tool

terminator 
xbacklight
wmctrl
fcitx-mozc


 xbacklight -set 10
 
 
wmctrl -xa terminator.Terminator || terminator




sudo add-apt-repository ppa:indicator-brightness/ppa

sudo apt-get update && sudo apt-get install indicator-brightness

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

