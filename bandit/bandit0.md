We need to login to bandit.labs.overthewire.org on port 2220 via ssh with username 'bandit0' and password bandit0

`ssh bandit0@bandit.labs.overthewire.org -p 2220`

type `yes` to accept fingerprint and enter

`ls` to show the files in the default directory which you can see is `/home/bandit0` if you type `pwd`

`cat readme`

The file is read and sent to stdout, displaying the password to the next level!

`exit`


