# Challenge name
Matching with *

## My solve
**Flag:** `pwn.college{wEZATpDz_MPHmgOFTf43AQiQ02r.QXxIDO0wiMwkjNzEzW}`

```bash
Connected!                                                                        
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
hacker@globbing~matching-with-:~$ cd /c*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{wEZATpDz_MPHmgOFTf43AQiQ02r.QXxIDO0wiMwkjNzEzW}
```

## Incorrect tangents I went on
None here

## What I learned
Globbing is quite the useful tool in minimising the amount we type. Here with *, globbing is done by essentially autofilling areas where * is detected, with wildcards that match the argument's properties(i.e the filename and pattern of argument). It also fills out filenames where * is detected except in instances where it replaces a leading '/' or a '.'

## References
Nothing to place here.
