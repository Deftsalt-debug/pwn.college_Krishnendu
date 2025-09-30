# Challenge name 
Backgrounding processes

## My solve
**Flag:** `pwn.college{gCnD_MTtH4CObE6bmA2PpJTJguv.QX3QDO0wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and 
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         138 S+   bash /challenge/run
root         140 R+   ps -o user=UID,pid,stat,cmd

I don't see a second me!

To pass this level, you need to suspend me, resume the suspended process in the 
background, and then launch a new version of me! You can background me with 
Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to 
do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~backgrounding-processes:~$ bg
[1]+ /challenge/run &
hacker@processes~backgrounding-processes:~$ 


Yay, I'm now running the background! Because of that, this text will probably 
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times 
to scroll this text out.
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and 
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         138 S    bash /challenge/run
root         148 S    sleep 6h
root         149 S+   bash /challenge/run
root         151 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:
pwn.college{gCnD_MTtH4CObE6bmA2PpJTJguv.QX3QDO0wiMwkjNzEzW}
```

## Incorrect tangents I went on
None to note here

## What I learned
The background builtin (bg) allows for processes to, titularly, run in the background. This allows for processes to carry on in the back while giving us access to the shell to invoke further processes or commands. We have also learnt the stat column of ps which is invoked by the -o flag. This characterises multiple states of the processes, assigning them to characters. A suspended process is signified by a T, an S states that a command is "sleeping", R states that a command is active (a + appended to this means that the process is in the foreground).

## References 
None here.