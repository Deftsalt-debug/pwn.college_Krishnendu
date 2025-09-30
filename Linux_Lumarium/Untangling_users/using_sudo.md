# Challenge name
Using Sudo

## My solve
**Flag:** `pwn.college{Aq3iw_kj1xPKN9Sg7ECIRty2haQ.QX4UDN1wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@users~using-sudo:~$ ls /
bin   challenge  etc   home  lib32  libx32  mnt  opt   root  sbin  sys  usr
boot  dev        flag  lib   lib64  media   nix  proc  run   srv   tmp  var
hacker@users~using-sudo:~$ sudo cat flag
pwn.college{Aq3iw_kj1xPKN9Sg7ECIRty2haQ.QX4UDN1wiMwkjNzEzW}
```

## Incorrect tangents I went on 
None here

## What I learned
Sudo is a modern day interpretation of su, without requiring any root passwords. It checks on policies listed from the root user to see if the command sudo runs is actually authorised and permitted. Su defaults into running the shell as the user it shifts to whereas the sudo command runs the specific command as the user it accesses. Sudo by default runs a command as the root user. It stands for subtitute user, do (as su does for substitute user)

## References 
None.