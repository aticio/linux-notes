[[file]] creation mask determines default [[Permission]]. If no mask were used, the default [[Permission]] will be 
* 777 for [[Directory]]es
* 666 for [[file]]s

umask command sets the [[file]] creation mask to mode, if given. You can use -S for symbolic notations.
*umask -S mode*

While chmod giving [[Permission]]s, the umask command will take away [[Permission]]s. For example 777 for chmod will give all [[Permission]]s but if you give unmask 777, it will remove all [[Permission]]s.

![[Pasted image 20220301013051.png]]

![[Pasted image 20220301013159.png]]