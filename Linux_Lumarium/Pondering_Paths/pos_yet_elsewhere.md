# Challenge name
Position yet elsewhere

## My solve
**Flag:** `pwn.college{EWBb3WwTsW2S9QP9tjbjhVGKUAK.QX4QTN0wiMwkjNzEzW}`

```bash
Connected!
hacker@paths~position-yet-elsewhere:~$ cd /
hacker@paths~position-yet-elsewhere:/$ /challenge/run
Incorrect...
You are not currently in the /usr/bin directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:/$ cd /usr/bin
hacker@paths~position-yet-elsewhere:/usr/bin$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{EWBb3WwTsW2S9QP9tjbjhVGKUAK.QX4QTN0wiMwkjNzEzW}
```

## Incorrect tangents I went on
There was an instance where I assumed that after shifting directory to /usr it would be possible to cd into /bin which was actually not a subdirectory of /usr but intstead of the root (/) directory. Quickly realised my error and passed the absolute path as an argument into cd 

## What I learned
Here we've accessed a subdirectory of a directory via cd, that being of /bin which is under /usr, it's iterative of the previous challenges but still essential to the use of cd, again used in cases where we have to access a file under multiple directories.

## References
None to be noted
