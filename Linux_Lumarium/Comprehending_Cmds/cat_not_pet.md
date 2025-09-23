# Challenge name
cat: Not the pet but the command!

## My solve
**Flag:** `pwn.college{gBuwPaf3Y4jiaV_CorU1AOZcQUU.QXxcTN0wiMwkjNzEzW}`

```bash
Connected!
hacker@commands~cat-not-the-pet-but-the-command:~$ cat /flag
pwn.college{gBuwPaf3Y4jiaV_CorU1AOZcQUU.QXxcTN0wiMwkjNzEzW}
```

## Incorrect Tangents I went on
None to report here

## What I learned
The 'cat' command is shorthand for contatenate, but it seems to do so much more in the command line. We observe it can output the contents of files if we pass an absolute path or the file name as its argument. If we were to list multiple files as a single argument it would simply conatenate them as one output (in simple words, just their contents as one output). If we were to also not pass any argument to it, it would output what the user inputs into the terminal. 

## References
None here