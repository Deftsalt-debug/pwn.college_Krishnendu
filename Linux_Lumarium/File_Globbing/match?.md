# Challenge name
Matching with ?

## My solve
**Flag:** `pwn.college{M8KFqGSIdvPERxUu0TTgLds0akP.QXyIDO0wiMwkjNzEzW}`

```bash
Connected!                                                                        
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{M8KFqGSIdvPERxUu0TTgLds0akP.QXyIDO0wiMwkjNzEzW}
```

## Incorrect tangents I went on
None to record this time.

## What I learned
Globbing with ? is almost identical to matching with *. Except with ? we can only match a singular character in the argument instead of multiple being used as a wildcard(as * does).

## References
None.