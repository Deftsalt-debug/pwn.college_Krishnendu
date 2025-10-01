# Challenge name
Groups and Files

## My solve
**Flag:** `pwn.college{Uy3Qf1-dd0v382CLT3CXQL4cvIW.QXxcjM1wiMwkjNzEzW}`

```bash 
Connected!                                                                        
hacker@permissions~groups-and-files:~$ chgrp hacker /flag
hacker@permissions~groups-and-files:~$ cat /flag
pwn.college{Uy3Qf1-dd0v382CLT3CXQL4cvIW.QXxcjM1wiMwkjNzEzW}
```

## Incorrect tangents I went on
None to place here.

## What I learned
An owner of a file can choose to share their files with specific users belonging to the owner's group. Groups are used to bottleneck and add a layer of specifics in accessing files/commands of the system by its users. Here the owner can modify the access specification of the file. This is what users in the group can do to the file (e.g. only being allowed to read the file). We can change the group of a file using the 'chgrp' command which takes in two arguments, the user we want to add to the group and the file which this specifies. If we have write access to the file and are in the group, chgrp generally requires root invokation. As a user we can also check what groups we are a part of using the id command, which lists the groups we are in as the current user.

## References 
None to note here.