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


HowToSetCapsLockAsCtrl

gnome-tweak-tool

theme

unity-tweak-tool

terminator 
xbacklight
xmctrl
fcitx-mozc


 xbacklight -set 10
 
 
wmctrl -xa terminator.Terminator || terminator




sudo add-apt-repository ppa:indicator-brightness/ppa

sudo apt-get update && sudo apt-get install indicator-brightness


ランチャーの『システム設定』をクリックして起動し、セキュリティとプライバシーをクリック、

「ファイルとアプリケーション」タブをクリック、ファイルとアプリケーションの利用状況を記録をクリックしてオフにする。

「検索」タブをクリック、Dashで検索するとき：オンラインの検索結果を含めるをオフにする。


$ gsettings set com.canonical.Unity.Lenses disabled-scopes "['more_suggestions-amazon.scope', 'more_suggestions-u1ms.scope', 'more_suggestions-populartracks.scope', 'music-musicstore.scope', 'more_suggestions-ebay.scope', 'more_suggestions-ubuntushop.scope', 'more_suggestions-skimlinks.scope']"

$ sudo apt-get remove unity-lens-video unity-scope-video-remote unity-lens-shopping unity-lens-music unity-lens-photos 

###TLP


 sudo add-apt-repository ppa:linrunner/tlp
 
 sudo apt-get update
 
 sudo apt-get install tlp tlp-rdw smartmontools ethtool


###PowerSavingTweaks for Intel Graphics


sudo nano /etc/default/grub

 GRUB_CMDLINE_LINUX_DEFAULT="intel_pstate=disable i915.lvds_downclock=1 drm.vblankoffdelay=1 i915.semaphores=1 i915_enable_rc6=1 i915_enable_fbc=1"

sudo update-grub

sudo apt install fcitx-mozc



sudo add-apt-repository ppa:chris-lea/node.js

sudo apt update

sudo apt install nodejs

npm xmas

node -v


With rc.local

This methods simply automatically applies during startup the technique used to change fnmode temporarily.

1. Edit the /etc/rc.local file.

gksudo gedit /etc/rc.local

2. Add this line near the end of the file, before the "exit" line:

echo 2 > /sys/module/hid_apple/parameters/fnmode

3. Reboot 



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

