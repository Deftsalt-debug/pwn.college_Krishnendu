# Challenge name
Hidden files

## My solve
**Flag:** `pwn.college{8J8tApPIM1rGUhC6ICY2_8LVocR.QXwUDO0wiMwkjNzEzW}`

```bash
Connected!
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.   .dockerenv           bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-3243029917361  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:/$ cat .flag-3243029917361
pwn.college{8J8tApPIM1rGUhC6ICY2_8LVocR.QXwUDO0wiMwkjNzEzW}
```

## Incorrect tangents I went on
I did not cd into the root directory and instead tried looking into the home directory which did not contain the flag file. 

## What I learned
This is the first instance where we are using options/flags with our commands these can be used to brute force and remove any limitations such as hidden files in this instance. This gives us a new layer of control and complexity to our commands and is used to enable/disable characteristics to our commands. Here we augment the -a flag with ls to list all the files under the directory, including the hidden files (files which start with a .) which linux hides by default. 