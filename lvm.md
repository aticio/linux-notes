Logical Volume Manager introduces extra layers of abstraction between the disks or storage devices presented to a Linux system and the [[file system]] placed on those devices.

You can create [[file system]] that extend across multiple storage devices. You can aggragate multiple storage devices into single [[logical volume]].

With lvm, you can extend or shrink [[file system]] in real-time.

You can migrate data frome one storage device to another while online.

You can  name your devices in human readable format.

Disk stripping: You can increase throughput by allowing you system to read data in parallel.

Data Mirroring is available.

You can take point-in-time snapshots of [[file system]]s.

Without lvm you would create a [[file system]] on a disk partition. But with lvm you create a [[file system]] on a [[logical volume]].


![[Pasted image 20220308125106.png]]

----------------------------------


Listing storage devices: *lvmdiskscan*


[[physical volume]] [[volume group]]