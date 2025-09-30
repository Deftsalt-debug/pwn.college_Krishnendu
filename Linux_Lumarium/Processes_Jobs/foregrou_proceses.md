# Challenge name
Foregrounding Processes

## My solve
**Flag:** `pwn.college{MnSBIsWmnDI220MhqDxWlZAL1Ah.QX4QDO0wiMwkjNzEzW}`

```bash
hacker@processes~foregrounding-processes:~$ /challenge/run
To pass this level, you need to suspend me, resume the suspended process in the 
background, and *then* foreground it without re-suspending it! You can 
background me with Ctrl-Z (and resume me in the background with 'bg') or, if 
you're not ready to do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~foregrounding-processes:~$ bg
[1]+ /challenge/run &
hacker@processes~foregrounding-processes:~$ 


Yay, I'm now running the background! Because of that, this text will probably 
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times 
to scroll this text out. After that, resume me into the foreground with 'fg'; 
I'll wait.

hacker@processes~foregrounding-processes:~$ fg
/challenge/run
YES! Great job! I'm now running in the foreground. Hit Enter for your flag!

pwn.college{MnSBIsWmnDI220MhqDxWlZAL1Ah.QX4QDO0wiMwkjNzEzW}
```

## Incorrect tangents I went on 
None to append here.

## What I learned
We can essentially allow and catalogue processes running in the background into the foreground. Note that to foreground a process means to make a process the active one on the shell. This is done by using the builtin fg when there is a background process running. 

## Refrerences
None.