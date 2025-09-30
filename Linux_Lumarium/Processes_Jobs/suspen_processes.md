# Challenge name
Sending Processes

## My solve
**Flag:** `pwn.college{MpxLzoIAhKC4ORa3DhInyyjfiRV.QX1QDO0wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         138     129  0 17:48 pts/0    00:00:00 bash /challenge/run
root         140     138  0 17:48 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can 
background me with Ctrl-Z or, if you're not ready to do that for whatever 
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         138     129  0 17:48 pts/0    00:00:00 bash /challenge/run
root         145     129  0 17:49 pts/0    00:00:00 bash /challenge/run
root         147     145  0 17:49 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{MpxLzoIAhKC4ORa3DhInyyjfiRV.QX1QDO0wiMwkjNzEzW}
```

## Incorrect tangents I went on
None here. 

## What I learned
Another way we can terminate/suspend processes in a less harsh manner and allows for it to be resumed in the shell. This is done by Ctrl+Z (Ctrl+Option+Z on macos). This is used to gain the terminal back during processes and allow for them to be resumed instead of being restarted.

## References
None to note.
