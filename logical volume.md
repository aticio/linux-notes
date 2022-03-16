![[Pasted image 20220310181123.png]]

Creating logical volume: *lvcreate -L 20G -n lv_data vg_app*
Listing logical volumes: *lvs*
Detailed logical volume info: *lvdisplay*
Creating a logical volume from remaining space: *lvcreate -l 100%FREE -n lv_logs vg_app*

For creating a mirrored logical volume: *lvcreate -m 1 -L 4G lv_secrets vg_safe*
1 here means 1 additional copy.
This will ensure that an exact copy of data will be kept in two storage devices.
There will be metadata subvolumes created at the same time. Check that: *lvs -a*
Removing logical volume *lvremove /dev/vg_safe/lv_secrets*

Then you can create a [[file system]] on top of logical volume.

----------------------

If you want to use remaining space in [[volume group]] want to create a logical volume you will get an insufficient free space error.

Each logical volumes divided by logical extents. Collection of logical extents consists a logical volume.

You can see logical extents with *lvdisplay* command. With *lvdısplay m* you can see a map view of logical extents. 

Just like logical extends, [[physical volume]] are consist of physical extents and there is a 1 to 1 ratio between logical and physical extents. You can see physical extents with *pvdısplay -m* 

There is a 4 MB space for logical volume metadata, and that space uses one physical extent. That is why you get insufficient free space error. You can see how many extents available with *vgdısplay* command.

You can either use this free extents number to create logical volume for remaining space with:

*lvcreate -l 511 -n lv_logs vg_app*

or you can use percents:

*lvcreate -l 100%FREE -n lv_logs vg_app*

------------------

Extended logical volume: *lvextend -L +5G -r /dev/vg_app/lv_data*
(-r is important here. Means resize. -r is used for extending the [[file system]]. You need to extend the [[file system]] as well while extending the logical volume) 

If you forgat resizing: resize2fs /dev/vg_app/lv_data