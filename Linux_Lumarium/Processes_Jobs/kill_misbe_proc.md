# Challenge name
Killling Misbehaving Processes

## My solve
**Flag:** `pwn.college{IxK5_CIm1vsHi4RRMWVvoGkcsXz.0FNzMDOxwiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@processes~killing-misbehaving-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 20:27 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-i
root           7       1  0 20:27 ?        00:00:00 /run/dojo/bin/sleep 6h
root         137       1  0 20:27 ?        00:00:00 /bin/bash /challenge/.init
root         138       1  0 20:27 ?        00:00:00 /bin/bash /challenge/.init
root         139       1  0 20:27 ?        00:00:00 su -c exec /challenge/decoy > /tmp/flag_fifo hacker
root         140     137  0 20:27 ?        00:00:00 sleep 6h
root         141     138  0 20:27 ?        00:00:00 sleep 6h
hacker       142     139  0 20:27 ?        00:00:00 /usr/bin/python /challenge/decoy
hacker       144       0  0 20:27 pts/0    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/
hacker       150     144  0 20:27 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       159     150  0 20:27 pts/0    00:00:00 ps -ef
hacker@processes~killing-misbehaving-processes:~$ kill 142
hacker@processes~killing-misbehaving-processes:~$ /challenge/run > /tmp/flag_fifo 
You're successfully redirecting /challenge/run to a FIFO at /tmp/flag_fifo! 
Bash will now try to open the FIFO for writing, to pass it as the stdout of 
/challenge/run. Recall that operations on FIFOs will *block* until both the 
read side and the write side is open, so /challenge/run will not actually be 
launched until you start reading from the FIFO!

hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo 
Sending the flag to /tmp/flag_fifo!
pwn.college{IxK5_CIm1vsHi4RRMWVvoGkcsXz.0FNzMDOxwiMwkjNzEzW}
```

## Incorrect tangents I went on
Here I was unexpectedly stuck on /challenge/run's process running infinitely, I have no idea why this is the case I assume the piping or rerouting of output to fifo is incorrect in the file. Eventually I used > to manually redirect output of /challenge/run into /fifo.

## What I learned
Here we use kill to remove a decoy process which impedes out objective of obtaining the flag. This is pretty reiterative of the previous chellenges only now we have to kill a process after lisning its PID. 

## References
None to record here.