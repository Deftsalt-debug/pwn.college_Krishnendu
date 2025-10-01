# Challenge name
Fun with group names

## My solve
**Flag:** `pwn.college{wgskEn-l0w107nkQlEyAftIdx1f.QXycjM1wiMwkjNzEzW}`

```bash 
Connected!                                                                        
hacker@permissions~fun-with-groups-names:~$ id
uid=1000(hacker) gid=1000(grp18128) groups=1000(grp18128)
hacker@permissions~fun-with-groups-names:~$ chgrp grp18128 /flag
hacker@permissions~fun-with-groups-names:~$ cat /flag
pwn.college{wgskEn-l0w107nkQlEyAftIdx1f.QXycjM1wiMwkjNzEzW}
```

## Incorrect tangents I went on
None to report here.

## What I learned
Conventionally in Linux, each user has their own titular group in which they are in, but in specific cases we can place a system's users all under a single group. This challenge is iterative of previous challenges but now requires us to use the id command to see what group (name being unknown to us) we are in a part of and chgrp into it to access /flag. 

## References
None.