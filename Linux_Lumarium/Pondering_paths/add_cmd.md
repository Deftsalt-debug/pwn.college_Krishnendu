# Challenge name
Adding commands

## My solve
**Flag:** `pwn.college{cxqyp_ok81QtrMjB-XIHAYWxCGV.QX2cjM1wiMwkjNzEzW}`

```bash
hacker@path~adding-commands:~$ nano win
hacker@path~adding-commands:~$ chmod a+x ~/win
hacker@path~adding-commands:~$ export PATH=~
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
pwn.college{cxqyp_ok81QtrMjB-XIHAYWxCGV.QX2cjM1wiMwkjNzEzW}
```

## Incorrect tangents I went on
This was a tough challenge, primarily due to my lack of competence with respect to setting PATH. Here instead of setting PATH to a directory I was stuck on passing the win script's absolute path into it, not allowing the bare command to be found or called at all. Here I had also forgot to add cat's path (found using which command) into the shell script which led to a few initial errors as well. I have also realigned permissions for win with chmod allowing executability which may have not been necessary. 

## What I learned
PATH can be used to set up bare calls to a completely fresh command at the expense (or not) of the rest of the commands under it. It is very volatile to any overwriting and can essentially render any command which isn't a shell builtin useless and incapable of any process. Here we utilise shell scripting to create win and knowledge of the which command to gain cat's absolute path in the system (as the overwriting of PATH would cause a deletion of every command's path in the system) to write into win. This can be counteracted by simply *adding* win's path into PATH instead of overwriting it or just using the read bultin instead of cat's path in the shell script. 

## References
None to note here.