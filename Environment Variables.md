Typically uppercase

To see:
echo $VAR_NAME 

[[PATH]] is a special one.

----------------------------------
For listing all environment variables: *printenv*
*printenv THE_VARIABLE* will give you the value of that environment variable
easy way is: *echo $THE_VARIABLE*

--------------------------------------
Creating environment variables: *export VAR="value"*
For removing: *unset VAR*

------------------------------
For persistent env vars put it in .bash_profile