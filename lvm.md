Logical Volume Manager introduces extra layers of abstraction between the disks or storage devices presented to a Linux system and the [[file system]] placed on those devices.

You can create [[file system]] that extend across multiple storage devices. You can aggragate multiple storage devices into single logical volume.

With lvm, you can extend or shrink [[file system]] in real-time.

You can migrate data frome one storage device to another while online.

You can  name your devices in human readable format.

Disk stripping: You can increase throughput by allowing you system to read data in parallel.

Data Mirroring is available.

You can take point-in-time snapshots of [[file system]]s.

![[Pasted image 20220308125106.png]]

----------------------------------
![[Pasted image 20220310181123.png]]

-----------------------------
Listing storage devices: *lvmdiskscan*

Creating physical volume: *pvcreate /dev/sdn*
Listing physical volumes: *pvs*

Creating volume groups: *vgcreate vg_app /dev/sdn*
Listing volume groups: *vgs*

Creating logical volume: *lvcreate -L 20G -n lv_data vg_app*
Listing logical volumes: *lvs*
Detailed logical volume info: *lvdisplay*
Creating a logical volume from remaining space: *lvcreate -l 100%FREE -n lv_logs vg_app*

Then you can create a [[file system]] on top of logical volume.
