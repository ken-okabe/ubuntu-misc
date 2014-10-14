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

```

