ubuntu-misc
===========

```
shortcut
wmctrl -xa terminator.Terminator || terminator



With rc.local

This methods simply automatically applies during startup the technique used to change fnmode temporarily.

1. Edit the /etc/rc.local file.

gksudo gedit /etc/rc.local

2. Add this line near the end of the file, before the "exit" line:

echo 2 > /sys/module/hid_apple/parameters/fnmode

3. Reboot 

UbuntuTips/Desktop/HowToSetCapsLockAsCtrl
対象とするUbuntuのバージョン

14.04 LTS
CapsLockキーを追加のCtrlキーとして使う方法を紹介します。

c
(i) GNOMEではgnome-tweak-toolを使うこともできます。

一度ログアウトし、再ログインします。





ランチャーの『システム設定』をクリックして起動し、セキュリティとプライバシーをクリック、

「ファイルとアプリケーション」タブをクリック、ファイルとアプリケーションの利用状況を記録をクリックしてオフにする。

「検索」タブをクリック、Dashで検索するとき：オンラインの検索結果を含めるをオフにする。


$ gsettings set com.canonical.Unity.Lenses disabled-scopes "['more_suggestions-amazon.scope', 'more_suggestions-u1ms.scope', 'more_suggestions-populartracks.scope', 'music-musicstore.scope', 'more_suggestions-ebay.scope', 'more_suggestions-ubuntushop.scope', 'more_suggestions-skimlinks.scope']"

$ sudo apt-get remove unity-lens-video unity-scope-video-remote unity-lens-shopping unity-lens-music unity-lens-photos 

```

