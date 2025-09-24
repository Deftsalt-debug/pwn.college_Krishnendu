# Challenge name
Making directories

## My solve
**Flag:** `pwn.college{8dtDkkBI6xQiHUVeHT62iRLyOze.QXxMDO0wiMwkjNzEzW}`

```bash
Connected!
hacker@commands~making-directories:~$ cd /tmp
hacker@commands~making-directories:/tmp$ mkdir pwn
hacker@commands~making-directories:/tmp$ cd ./pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{8dtDkkBI6xQiHUVeHT62iRLyOze.QXxMDO0wiMwkjNzEzW}
```

## Incorrect tangents I went on
None to note here

## What I learned
mkdir unlocks us a realm of the creation of directories, similar to touch in that sense but scaled up to create directories. The command creates empty containers under the directory we call it from or the absolute path of the directory we want to create. This chalenge also incorporated the use of touch and cd'ing as normal.

## References 
None