![[Pasted image 20220301010402.png]]

--------------------------------------------
![[Pasted image 20220301010540.png]]

If [[Directory]] doesn't have enough permission for needed action, you can't do it.


--------------------------------------------------

![[Pasted image 20220301010624.png]]
[[Group]]

--------------------------------------

![[Pasted image 20220301010915.png]]

------------------------------

For example:
Giving permission to user and [[Group]]:
*chmod u=rwx,g=rw sales.data*

Adding permission to [[Group]]:
*chmod g+x sales.data*

-----------------------------------------

![[Pasted image 20220301011623.png]]

Example:
![[Pasted image 20220301011750.png]]

![[Pasted image 20220301011805.png]]

----------------------------------

[[file]] creation mask determines default [[Permission]].

------------------

When a process is started, it runs using the starting user's UID and GID
setuid = Set User ID upon execution.
setuid forces the process to start with the owners id.

![[Pasted image 20220317181948.png]]
You will see s letter on the execution permition of the owner place. This process will be executed as root regardles of who executes it.

setuid files are an attack surface and they are not honored on shell scripts.

![[Pasted image 20220317182215.png]]

![[Pasted image 20220317182345.png]]
![[Pasted image 20220317182432.png]]

Best option for editing setuid files is editing by its owner. Which means the best permission will be 4755.

--------------------

setgid = Set Group ID upon execution. It allows to run the file with the group privilages of the file rather than the gorup privilages of the executer's group.

![[Pasted image 20220317183254.png]]

![[Pasted image 20220317183440.png]]

![[Pasted image 20220317183800.png]]
![[Pasted image 20220317183842.png]]

------------------------

The Sticky Bit permission only allows owner of the file to delete it.

![[Pasted image 20220317184256.png]]

You can checkout the t letter at the execution filed of the directory. It will be applicable for files have 777 permissions.

![[Pasted image 20220317184410.png]]

![[Pasted image 20220317184507.png]]