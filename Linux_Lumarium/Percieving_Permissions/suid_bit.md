# Challenge name 
The SUID bit

## My solve
**Flag:** `pwn.college{IRZVfXDVxDmdOQJxppCT3N__tYb.QXzEjN0wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@permissions~the-suid-bit:~$ chmod u+s /challenge/getroot 
hacker@permissions~the-suid-bit:~$ /challenge/getroot 
SUCCESS! You have set the suid bit on this program, and it is running as root! 
Here is your shell...
root@permissions~the-suid-bit:~# cat /flag
pwn.college{IRZVfXDVxDmdOQJxppCT3N__tYb.QXzEjN0wiMwkjNzEzW}
```

## Incorrect tangents I went on
None to note here.

## What I learned
The SUID bit being enabled in a file or executable is sort of a pesudo-sudo, it allows for us as an external user to operate on the file or executable as the owner only (usually root here), for that instance, if we have the specific perms for it. Here the perms for an SUID bit would be an 's' in place of the executable in the access string in the file/executable's long listing, meaning that the program is accessable by SUID. Therefore with SUID, as long as any user has perms for execution by the owner, they can execute the file/executable as the owner. 

## References
None here.