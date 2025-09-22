# Challenge name
The Root

## My solve
**Flag:** `pwn.college{Ep7Vu5I1bdVAxSxJt0DsfChbUmx.QX4cTO0wiMwkjNzEzW}`

```bash
Connected!
hacker@paths~the-root:~$ ./pwn
bash: ./pwn: No such file or directory
hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{Ep7Vu5I1bdVAxSxJt0DsfChbUmx.QX4cTO0wiMwkjNzEzW}
```

## Incorrect tangents I went on
Here instead of using the root directory, I accessed the current directory, whose path did not exist. 
Immediatly course correcting by opening the actual path of root directory containing the file

## What I learned 
This was an essential element of navigation in the terminal and file system of a computer, accessing and utilising the root directory is fundamental 
in daily operation and is further built upon in memory architecture through various sub-directories whom we anchor to the root directory.   

## References
pwn.college youtube: Linux Luminarium - 2 The File System video
