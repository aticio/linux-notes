[[Shell]] scripts

Shebang defines the interpreter of that sh file.
Example: *#!/bin/bash*

If shebang is not supllied, the script will use using your shell. It is better to use it anyway.

You can use other executers like python as shebang:
*#!/usr/bin/python*

Variables Example:
VARIABLE_NAME="Value"
MAke sure there are no spaces around = sign

By convention, variable names are all upper case.

If you want yo use variable with a string let's say, you need to put it into curly braces:

*echo This is ${MY_NAME}'s computer'.

You can define an output of a command as a variable like:
*SERVER_NAME=$(hostname)*

![[Pasted image 20220318121143.png]]

-----------------

You can create tests (like conditions):
Example:

[ -e /etc/passwd ]

If the file exists it will return 0 (True).

![[Pasted image 20220318121553.png]]

![[Pasted image 20220318122038.png]]

----------------------------

If statements:
![[Pasted image 20220318123107.png]]


Inside the condition you need to use one = sign for equality comparison and make sure to leave a blank space around the = sign.

Example:
*if [ "$MY_SHELL" = "bash" ]
then
	command
fi*

------------------
for loops:

![[Pasted image 20220318124025.png]]

you can also put the list in a variable like:

![[Pasted image 20220318124109.png]]

--------------

![[Pasted image 20220318124247.png]]

---------------------------

Reading user input:

![[Pasted image 20220318124537.png]]

