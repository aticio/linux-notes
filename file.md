Linux represents practically everything as a file.

**Comparing files**
![[Pasted image 20220302175920.png]]

![[Pasted image 20220302180312.png]]

----------------------------
*file file_name* displays the file type

---------
*strings file_name* shows printable text in binary files.

-------------------------
Cutting data from a file: (d means delimeter. In this example it is (:). Get first and fifth column)
*cut -d: -f1,5 file_name*

---------------------------------------------
For translating character of a given output:

*cat ozgur.txt | tr ":" "-"*

---------------------------------------------
Showing the output in table format:

*column -t*
