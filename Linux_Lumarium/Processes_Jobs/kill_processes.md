# Challenge name
Killing processes

## My solve
**Flag:** `pwn.college{EBTZ_vKaYFJCXzF1wgVUss-vEyo.QXyQDO0wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@processes~killing-processes:~$ ps -e | grep dont_run
hacker@processes~killing-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 20:57 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo/bin/sleep 6h
root           7       1  0 20:57 ?        00:00:00 /run/dojo/bin/sleep 6h
root         135       1  0 20:57 ?        00:00:00 su -c /challenge/.launcher hacker
hacker       136     135  0 20:57 ?        00:00:00 /challenge/dont_run
hacker       137     136  0 20:57 ?        00:00:00 sleep 6h
hacker       139       0  0 20:57 pts/0    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/bin/bash /run/dojo/bin/ssh-entrypoint
hacker       145     139  0 20:57 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       156     145  0 20:58 pts/0    00:00:00 ps -ef
hacker@processes~killing-processes:~$ kill 136
hacker@processes~killing-processes:~$ /challenge/run 
Great job! Here is your payment:
pwn.college{EBTZ_vKaYFJCXzF1wgVUss-vEyo.QXyQDO0wiMwkjNzEzW}
```

## Incorrect tangents I went on
Here I passed an incorrect argument into grep, it should've been /challenge/don't_run with the -ef flag, The second process I initiated is a more inefficient method.

## What I learned
The kill process allows for us to pinpoint a specific program executing and terminate it swiftly through its PID. The PID of the process is obtained from the ps -ef command which lists the processes' individual PID's. Kill takes in the numeric PID of the process as an argument and subsequently eliminates it from running, thus no longer being present under ps. 

## References
None here.