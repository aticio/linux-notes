RPM distros: RHEL, CentOS and Oracle Linux.

---------------------------
For RHEL 7 - CentOS 7 and earlier *yum is used*

For searching [[package]]:
*yum search string*

For info about [[package]]:
*yum info package*

For installing:
*yum install (-y) package*

For removing:
*yum remove package*

For updating:
*yum upgrade (package)*

----------------------------------------

For RHEL 8 - CentOS8 dnf become the standart

For searching [[package]]:
*dnf search string*

For info about [[package]]:
*dnf info package*

For installing:
*dnf install (-y) package*

For removing:
*dnf remove package*

For updating:
*dnf upgrade (package)*

*dnf autoremove* will clean all unused dependencies.

---------------------------
rpm command won't install all dependencies.
Check for [[Linux Distro]] and cpu architecture. 
If the rpm package says no arch, meaning there is no specific architecture requirement.
You can use *uname -m* to see your machines architecture.

For downloading file you can use *curl*
If you use -O parameter, the package will be saved as the same name as it is given on the internet:

*curl -O https://somepackage.rpm *
