Basic Input Output System.

Boot loaders start the operating system.
	- LILO - Linux Loader
	- GRUB - Grand Unified Bootloader

intrd - initial RAM disk.

/boot contains required files to boot Linux
	- initrd
	- kernel [[Linux Kernel]]
	- boot loader configuration

Kernel Ling Buffer:
	- Contains messages from the [[Linux Kernel]]
	- /var/log/dmesg

Runlevels:
![[Pasted image 20220304164017.png]]

Runlevels traditionally controlled bay init program configured in /etc/inittab. [[etc]]

Systemd takes place of runlevels:
	- Uses targets instead of runlevels
	- systemctl is used to control systemd
		- *systemctl set-default graphical.target*

-----------------------
For rebooting: *reboot*
For shutdown: shutdown (options) time (message):
	*shutdown -r now*
	*shutdown -r +5 "rebooting soon"*
	*shutdown -r 15:30 "rebooting"*

For poweroff: *poweroff*