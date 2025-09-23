# Challenge name
Touching files

## My solve
**Flag:** `pwn.college{Mgwfy4qne6DRbwRZHNGCo1AMCyI.QXwMDO0wiMwkjNzEzW}`

```bash
Connected!
hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ touch college
hacker@commands~touching-files:/tmp$ /challenge/run
Success! Here is your flag:
pwn.college{Mgwfy4qne6DRbwRZHNGCo1AMCyI.QXwMDO0wiMwkjNzEzW}
```

## Incorrect tangents I went on
None to report

## What I learned
This challenge requires us to use touch to create two files from /tmp, touch is another important command which we use to create files, the fundamental to a system. Here we pass an argument to touch so as to give the filename of the file it is creating, touch makes the file under the current directory we are in. 

## References 
None to note here