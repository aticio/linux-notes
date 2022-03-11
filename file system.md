Before a [[partition]] can be used by a linux system, it needs a file system.

ext = Extended file system
ext2, ext3, ext4

Creating file system:

*mkfs -t TYPE DEVICE*

Example:
*mkfs -t ext3 /dev/sdb2*

---------------------------------

You can mount a [[mount point]] to the file system.

