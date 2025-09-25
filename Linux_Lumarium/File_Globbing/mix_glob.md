# Challenge name
Mixing Globs

## My solve
**Flag:** `pwn.college{ckjQbC1QTPPkLBnNSsYq0mpBFd6.QX1IDO0wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@globbing~mixing-globs:~$ cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run *c*e*p*
Error: you did not use a square bracket glob...
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{ckjQbC1QTPPkLBnNSsYq0mpBFd6.QX1IDO0wiMwkjNzEzW}
```

## Incorrect tangents I went on
Here I had initially used a * glob instead of the desired square globs, although my approxiation is that the * globs would have sufficed here too.

## What I learned
This was more of a compressed version combining all we've learnt from the previous challenges, i.e matching with * and [] to get a desired, unknown file through wildcarding. This consists of the usage of two globs, the [] and * from which we get the desired characters from the set inside [] and the rest of the filename is approximated/wildcarded by the * glob. 

## References 
None to note here.