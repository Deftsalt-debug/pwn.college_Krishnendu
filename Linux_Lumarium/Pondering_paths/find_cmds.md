# Challenge name
Finding commands

## My solve 
**Flag:** `pwn.college{8QTbLjGt4nOGQOPj5Ibtpwzk5s4.01NzEzNxwiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@path~finding-commands:~$ which win
/challenge/paths/234/win
hacker@path~finding-commands:~$ cat /challenge/paths/234/flag
pwn.college{8QTbLjGt4nOGQOPj5Ibtpwzk5s4.01NzEzNxwiMwkjNzEzW}
```

## Incorrect tangents I went on
None to report here.

## What I learned
The which command allows us to peek into PATH's contents, peering into the expanse of the directories where all our commands of the shell (except builtins) reside and allow for themselves to be called by their bare name in the shell. The which command allows for us to pass a specific command for which it'd search the PATH database for a path that exactly matches the shell's knowledge of the bare name of the command. 

## References
None to note here.