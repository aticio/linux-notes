Creating volume groups: *vgcreate vg_app /dev/sdn*
You can also create volume groups with two [[physical volume]]:
*vgcreate vg_safe /dev/sdd /dev/sde*
Listing volume groups: *vgs*
If you want to remove a [[physical volume]] from a volume group:
*vgreduce vg_safe /dev/sde*
Removing volume group: *vgremove vg_safe*


----------------------------------------

If you want to extend the space of a volume group, first create a [[physical volume]] from a free disk.

Then:

Extending volume groups: *vgextend vg_app /dev/sdc*

