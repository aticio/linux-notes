Changing user: *su username*
*whoami* will give current account

If you use su with "-", you will get the environment of changed user. Your [[Environment Variables]] won't passed.

--------------------

*sudo*  - You can execute command as another user, mostly [[root]].

Good thing to use sudo is, you don't need to know the password of the other user. If sudo comfiguration permits access, you can go on. Sysadmins would arrange that.

-----------------------------------

*sudo -u user* to select specific user.
Only *sudo command* will execute as [[root]]

----------------------

*visudo* will edit the /etc/sudoers file for changing sudo configuration.