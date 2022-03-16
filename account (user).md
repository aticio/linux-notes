accounts have:
username
UID
default [[Group]]
comments
[[Shell]]
[[home]] directory 

all this info stored in [[etc]]/passwd file.

Format of /[[etc]]/passwd:
username:password:UID:GID:comments:home_dir:shell

Usernames are case sensitive.
By convention use all lowercase.
It's a custom to use less than 8 characters.

[[etc]]/passwd file is readable by every user.

Encrypted passwords are stored in /[[etc]]/shadow file and it's only readable by [[root]]

[[root]] has always the UID 0.

System accounts have UIDs < 1000.

Adding user: *useradd (options) username*
-c Comment
-m Create the home directory
When you use -m, contents of /etc/skel will be copied to home directory. This typically contains [[Shell]] configuration.

-s /shell/path The path of user's [[Shell]]
If you want the user not to be logged in (like app user):
set shell to /usr/sbin/nologin
-g Specify default gorup
-G Group1,GroupN Specify additional [[Group]]s
-r Create a system account
-d /home/dir Specify the [[home]] directory.
-u setting the UID.
It is a common practice to use same UID across multiple systems.

Example:
*useradd -c "Ozgur Atici" -m -s /bin/bash -g admins -G montior appuser*


Creating a password:
*passwd ozgur*

Deleting user: *userdel (-r) username*
-r is for deleting [[home]] directory.

Updating an existing account: *usermod (options) username*
-c Comments
-g group
-G Group1,GroupN additional [[Group]]s
-s /shell/path Path to user's [[Shell]]