# Challenge name
Position thy self

## My solve
**Flag:** `pwn.college{02eWiC6rD4LjGFACnBSwCNoNGtD.QX2QTN0wiMwkjNzEzW}`

```bash
Connected!
hacker@paths~position-thy-self:~$ cd /challenge
hacker@paths~position-thy-self:/challenge$ /challenge/run
Incorrect...
You are not currently in the /sys directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:/challenge$ cd /sys
hacker@paths~position-thy-self:/sys$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{02eWiC6rD4LjGFACnBSwCNoNGtD.QX2QTN0wiMwkjNzEzW}
```

## Incorrect Tangents I was on
This was a doozy, here I tried using 'ls' to show me what was present in the root and challenge directories expecting to see an executable yet it only lead me to further directories. From here it was a 10 minuite guess game of how to execute the given challenge file which only yeilded, "no such directories exist" from bash. This eventually was deciphered by me figuring out that I fixated on **cd** far too much, to an extent that made me assume that the cd into path would somehow also execute my program. My error being that I hadn't even executed the file to understand where to further proceed. Shortly fixed soon after I figured that 'cd' wasn't my way out. 

## What I learned
cd is NOT going to ever execute files, it acts more as a bridge in between directories and presents navigation across the file systems by the manner of absolute paths. To execute, we will eventually have to use the absolute path to the file after navigating into the correct directory (this is /sys in my question)

## References
None, had a quick look over this to clear understanding after realising my error https://bash.cyberciti.biz/guide/Cd_command
