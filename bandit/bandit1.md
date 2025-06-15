We now need to login as bandit1

`ssh bandit1@bandit.labs.overthewire.org -p 2220`

We have a file named - which doesn't seem to open when we use the `cat` command.

The top answer on stackoverflow for "how to open a dashed filename using terminal" says:

"This type of approach has a lot of misunderstanding because using - as an argument refers to STDIN/STDOUT i.e dev/stdin or dev/stdout .So if you want to open this type of file you have to specify the full location of the file such as ./- .For eg. , if you want to see what is in that file use cat ./-"

`cat ./-`

This gives us the password to the next level!

`exit`
