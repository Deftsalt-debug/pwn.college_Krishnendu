# Challenge name
Listing processes

## My solve
**Flag:** `pwn.college{wdujt8jHqWs1tRwcxjLIxt5V6Di.QX4MDO0wiMwkjNzEzW}`

```bash
hacker@processes~listing-processes:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.2  0.0   1056   640 ?        Ss   20:45   0:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo/bin/sleep 6h
root           7  0.1  0.0 231708  2560 ?        S    20:45   0:00 /run/dojo/bin/sleep 6h
root         132  0.0  0.0   4132  2560 ?        S    20:45   0:00 /challenge/4414-run-3915
root         135  0.0  0.0   2744  1600 ?        S    20:45   0:00 sleep 6h
hacker       137  0.1  0.0 231576  3520 pts/0    Ss   20:45   0:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/bin/bash /run/dojo/bin/ssh-entrypoint
hacker       143  0.0  0.0 231940  4160 pts/0    S    20:45   0:00 /run/dojo/bin/bash --login
hacker       153  0.0  0.0 233600  3840 pts/0    R+   20:45   0:00 ps aux
hacker@processes~listing-processes:~$ /challenge/4414-run-3915
Yahaha, you found me! Here is your flag:
pwn.college{wdujt8jHqWs1tRwcxjLIxt5V6Di.QX4MDO0wiMwkjNzEzW}
```

## Incorrect tangents I went on
None to note here

## What I learned
To list processes running under the shell, was use the command ps suffixed with -ef or aux to hand us more data compared to a minute amount ps itself gives us. -ef flag is standard syntax where e lists every output and f does the listing under full format, the -ef argument also provides an additional Parent Process ID (PID) of the processes. Suffiing aux also gives us the similar values as -ef but instead of PID, it outputs the percentage of total system CPU and Memory that the process is utilizing.

## References
None here.
