/etc/fstab - The File System Table [[file system]] - [[etc]]
Controls what devices get mounted and where on boot
Each entry is made up of 6 fileds
	- device
	- mount point
	- file system table
	- mount options
	- dump
	- fsck order

If fsck order is 0 it is not going to be checked. If it is 1, it is going to be checked first and goes on.