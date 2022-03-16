Creating physical volume: *pvcreate /dev/sdn*
Listing physical volumes: *pvs*
For removing physicla volume: *pvremove /dev/sde*

For migrating from one physical volume to another: *pvmove /dev/sdb /dev/sde*
But initially you need to create a new physical volume. Then put it into the existing [[volume group]]: *vgextend vg_app /dev/sde*