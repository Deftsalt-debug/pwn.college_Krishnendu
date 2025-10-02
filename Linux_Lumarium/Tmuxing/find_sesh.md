# Challenge name
Finding sessions

## My solve
**Flag:** `pwn.college{sAZhBQ1z8j7QMGxOziUODa_klbV.01N4IDOxwiMwkjNzEzW}`

```bash
hacker@terminal-multiplexing~finding-sessions:~$ screen -ls
There are screens on:
	144.session_993858e8ab532536	(Detached)
	147.session_43a2acf23f91678b	(Detached)
	150.session_72eac3ca315faf75	(Detached)
3 Sockets in /home/hacker/.screen.
hacker@terminal-multiplexing~finding-sessions:~$ screen -r 147
[screen is terminating]
hacker@terminal-multiplexing~finding-sessions:~$ screen -r 150
[screen is terminating]
hacker@terminal-multiplexing~finding-sessions:~$ screen -r 144
[detached from 144.session_993858e8ab532536]
```

## Incorrect tangents I went on
None here.

## What I learned
We can see all active sessions by passing -ls as a flag to screen. This lists all PIDs and identifiers of active screens. To reattach to a specific screen, we can pass its PID or name as an argument into screen -r. 

## References
None to note here.