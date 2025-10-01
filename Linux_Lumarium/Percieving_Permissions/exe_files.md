# Challenge name
Executable files

## My solve
**Flag:** `pwn.college{o53fi_h-KG1vuDiot4ZMg-BN238.QXyEjN0wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@permissions~executable-files:~$ id
uid=1000(hacker) gid=1000(hacker) groups=1000(hacker)
hacker@permissions~executable-files:~$ ls -l /challenge/run
-r--r--r-- 1 hacker hacker 32 Jan 14  2025 /challenge/run
hacker@permissions~executable-files:~$ chmod go+x /challenge/run
hacker@permissions~executable-files:~$ /challenge/run
bash: /challenge/run: Permission denied
hacker@permissions~executable-files:~$ chmod a+x /challenge/run
hacker@permissions~executable-files:~$ /challenge/run
Successful execution! Here is your flag:
pwn.college{o53fi_h-KG1vuDiot4ZMg-BN238.QXyEjN0wiMwkjNzEzW}
```

## Incorrect tangents I went on
Here I assumed we were acting as part of the owner group or as the other users while acting on /challenge/run and tried to only modify those parameters to being executable on /challenge/run. It appears that my premonition was incorrect and we were accessing /challenge/run from the owner user's shell. 

## What I learned
This was reiterative of the previous challenge, continuing with chmod to modify perms but now enacting on commands/executables. Here to run the command we have to enable executable perms(x) via chmod. 

## References 
None to note here.