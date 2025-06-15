`ssh bandit4@bandit.labs.overthewire.org`

`ls` gives us a directory called `inhere`

`cd inhere`

`ls -la`

We get 10 files labelled -file00 to -file09

The clue for the level is "The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command."

Unlike windows, linux doesn't rely on file extensions to determine the type of content of a file. Instead we can use the file command and a wildcard to pattern match all our files.

We could try

`file *` but this won't work as we learned in a previous level that dashed filenames are handled differently.

`file ./*` gives the output:

```text
./-file00: PGP Secret Sub-key -
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data
```

So now we just output it to stdout with cat using the relative path:

`cat ./-file07`

And we get the password!
