`ssh bandit4@bandit.labs.overthewire.org -p 2220`

`ls` shows a directory called `inhere`

`cd inhere` to change to that directory

ls -la shows 

`ls -la
total 12
drwxr-xr-x 2 root    root    4096 Apr 10 14:23 .
drwxr-xr-x 3 root    root    4096 Apr 10 14:23 ..
-rw-r----- 1 bandit4 bandit3   33 Apr 10 14:23 ...Hiding-From-You`

Hmm how are we going to open this file? We can see that the owner is bandit4, the group is bandit3, and the owner has rw (read and write) permissions and the group has r (read) permissions.

We should be able to read this file, let's copy paste it exactly and output it to stdout using cat:

`cat ...Hiding-From-You`

And BOOM! We get the password!
