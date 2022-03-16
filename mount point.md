A [[Directory]] used to access the data on a [[partition]]

/(slash) is always a mount point

![[Pasted image 20220307151404.png]]

-------------------
You can have mount points on mount points
/home
/home/ozgur

-------------------------------------------

Mounting with mount:

*mount /dev/sdb3 /opt*

----------------------
Manuel mounts do not persists. If you want to make mounts persist between reboots, add an entry in the /etc/fstab. [[etc]] [[fstab]]

After adding a record to [[fstab]], for mounting just type *mount /app*. It will read the [[fstab]] and get the necessary information from the file.

---------------------------------------

Unmounting with the umount command

*umount DEVICE_OR_MOUNT_POINT*

Example:
*umount /opt*
*umount /dev/sdb3*


After that if necessary you can remove logical volume.

-----------------------------------
Preparing swap space:
*mkswap /dev/sdb1*

enabling swap partition:
*swapon /dev/sdb1*

swpas in use:
*swapon -s*

----------------------
Adding label (opt) to device:
*e2label /dev/sdb3 opt*