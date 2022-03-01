*-name pattern* -> find [[file]]s and [[Directory]]es matching the pattern
*-iname pattern* -> ignore case
*-ls* -> Performs an ls on each of the found items
*-mtime days* ->  find [[file]]s that are days old
*-size num* -> find [[file]]s that are of size num
*-newer file* -> find [[file]]s that are newer than [[file]]s
*-exec command {} \;* -> Run commands for all [[file]]s that are found

--------------------------------------------
Another faster version of find is [[locate]]