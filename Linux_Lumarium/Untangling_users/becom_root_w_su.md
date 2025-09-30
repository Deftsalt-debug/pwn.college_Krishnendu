# Challenge name
Becoming root with su

## My solve
**Flag:** `pwn.college{gWipPkW72LpfaJgYbtRm1pcKsYM.QX1UDN1wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@users~becoming-root-with-su:~$ su
Password: 
root@users~becoming-root-with-su:/home/hacker# ls
COLLEGE  Desktop  PWN  a  flag  instructions  myflag  not-the-flag  pwn  stdout  the-flag
root@users~becoming-root-with-su:/home/hacker# cat flag
pwn.college{gWipPkW72LpfaJgYbtRm1pcKsYM.QX1UDN1wiMwkjNzEzW}
```

## Incorrect tangents I went on
None to report here.

## What I learned 
The root is used to refer to the system administrator under the linux hierarchy. 'Su' is an older command used to ascend to the root access. Running it usually requires a root password which is, in the modern age, obsolete. The SUID (Set User ID) bit, which su has and runs in, is a unique flag in linux that allows/permits a file to be executed with the privileges of the file's owner(here being the root user).

## References
None to note here.
