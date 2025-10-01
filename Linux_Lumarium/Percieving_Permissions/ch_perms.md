# Challenge name
Changing perms

## My solve
**Flag:** `pwn.college{QC_MH-hdBusy4h8aspFuffcINLB.QXzcjM1wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@permissions~changing-permissions:~$ id
uid=1000(hacker) gid=1000(hacker) groups=1000(hacker)
hacker@permissions~changing-permissions:~$ chmod o+r /flag
hacker@permissions~changing-permissions:~$ cat /flag
pwn.college{QC_MH-hdBusy4h8aspFuffcINLB.QXzcjM1wiMwkjNzEzW}
```

## Incorrect tangents I went on 
None to report on this front

## What I learned
This discussed exactly what I wrote in the previous challenge, we delve into the specific file id that gives us a look at its permissions for accessing with regards to it's user(u), groups(g) and world(o). Here when we ls -l, i.e. long list a file, we get an idea of its perms from a 10 bit string of characters, the first giving an idea of the file type and the other nine giving the permissions to the user, user's group and other users in the system as previously said. The chmod command allows for us as the owner to change the permissions of specific (or all) entities of the file. Here chmod takes in two arguments one being the MODE and FILE, this mode is specified by either modifying an existing permission or creating a wholly new one overwriting the old perm. To modify an existing mode we need to pass it as a WHO(+/-)WHAT format, which defines who as the specific user/group which we are modifying the perms of(u,g,o or a); The WHAT here is the specific perm we want to add or delete, (w,x,r). A user usually requires the write access to a file to modify its perms using chmod. 

## References 
None.