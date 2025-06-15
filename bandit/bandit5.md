`ssh bandit5@bandit.labs.overthewire.org -p 2220`

`ls` shows we have a directory called `inhere`

`cd inhere`

`ls`

```text
maybehere00  maybehere04  maybehere08  maybehere12  maybehere16
maybehere01  maybehere05  maybehere09  maybehere13  maybehere17
maybehere02  maybehere06  maybehere10  maybehere14  maybehere18
maybehere03  maybehere07  maybehere11  maybehere15  maybehere19
```

The clue tells us:

The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

    human-readable
    1033 bytes in size
    not executable

Commands you may need to solve this level

ls , cd , cat , file , du , find

My strategy here would be to find all files that are 1033 bytes in size to narrow down our search and take it from there.

A google search to "find files of a particular size in linux" tells us we can use the find command with the -size flag followed by the size and the unit. c happens to specify bytes.

We'll search everything so we just use * to match all the directories.

`find * -size 1033c`

this outputs

`maybehere07/.file2` to the terminal.

Seems like there is only one file that matches this criterion!

`cat maybehere07/.file2`

And we get our password!

`exit`
