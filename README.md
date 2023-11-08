# Volume keys (Fn+F7 & Fn+F8) fix

Request superuser access
~~~bash
sudo su
~~~

Download the config
~~~bash
wget -q https://github.com/franklin-albuquerque/ubuntu_volume-keys-fix/raw/main/hwdb.d/61-keyboard-local.hwdb -O /etc/udev/hwdb.d/61-keyboard-local.hwdb
~~~

Update the hardware database for udev
~~~bash
systemd-hwdb update
udevadm trigger /dev/input/event3
~~~

Restart the system to apply the changes
~~~bash
reboot
~~~
