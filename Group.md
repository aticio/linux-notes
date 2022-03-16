* Every [[account (user)]] is in at least one group.
* [[account (user)]] can belong to many groups.
- *groups* command displays a [[account (user)]]'s groups.
- You can also use id -Gn
- *chgrp* command will change the gorup.

Group details are stored in /[[etc]]/group 
Format of the file is:
group_name:password:GID:account1,account2

To display the groups of a user:
*groups username*

To create a group: *groupadd (options) group_name*
-g Specify GID

To delete a group: *groupdel groupname*

Change the properties of an existing group: *groupmod (options) group_name*
-g GID Change the GID
-n GROUP Rename the group

