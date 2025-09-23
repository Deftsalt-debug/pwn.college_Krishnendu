# Challenge name
Position Elsewhere

## My solve
**Flag:** `pwn.college{ku34_lzFkwfTybQqlvCaAbeOcg9.QX3QTN0wiMwkjNzEzW}`

```bash
Connected!
hacker@paths~position-elsewhere:~$ cd /challenge
hacker@paths~position-elsewhere:/challenge$ /challenge/run
Incorrect...
You are not currently in the /etc directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:/challenge$ cd /etc
hacker@paths~position-elsewhere:/etc$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{ku34_lzFkwfTybQqlvCaAbeOcg9.QX3QTN0wiMwkjNzEzW}
```

## Incorrect Tangents I was on
None here, reiterative as the previous challenge

## What I learned
We can essentially execute '/challenge/run' absolute path anywhere, including the root directory for the system to subsequently (I suppose as a failsafe) tell us where exactly we must change directory to. Reiterating, the cd command is SOLELY to take arguments of paths and switch directories to the exact path, whether we want to execute the program in the 'new' changed directory is up to us. 

## References
None here