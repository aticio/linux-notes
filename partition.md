Disks can be divided into parts, called partitions.

------------------------

Master Boot Record - MBR is a boot sector at the beginnig of a storage device. Coontains information on ho the logical partitions are organized on the disk.

GPT or GUID Partition Table is replacing MBR. This supports up to 128 partitions. Not supported by older os'es.

--------------------

fdisk is the main tool for creating pratitions.

*fdisk /path/to/device*

Listing partitions:
*fdisk -l*

Creating new partitions:
*fdisk -n* and commands goes on.
