# Challenge name
Reading Manuals

## My solve
**Flag:** `pwn.college{sJih-KcM9BPSBmvook5VIpMRwZG.QX0EDO0wiMwkjNzEzW}`

```bash 
Connected!                                                                        
hacker@man~reading-manuals:~$ man challenge
hacker@man~reading-manuals:~$ /challenge/challenge --sihcmv 950
Correct usage! Your flag: pwn.college{sJih-KcM9BPSBmvook5VIpMRwZG.QX0EDO0wiMwkjNzEzW}
```

## Incorrect tangents I went on 
None to note here

## What I learnt
The man command allows for us to access built in documentation of the various commands in the terminal, all formatted in a specific order with its name, synopsis, description as well as metadata about its authors, collections etc. This module required us to read over the manual of the challenge command and figure out what exact argument we should pass along with challenge to obtain the flag. Note that man does not take absolute paths of commands (ex. /usr/bin/yes) and instead returns garbage values. 

## References 
None to report here.
