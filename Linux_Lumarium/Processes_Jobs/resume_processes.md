# Challenge name 
Resuming processes

## My solve
**Flag:** `pwn.college{s0XT2PneDuxhSUzVnHBbct6YF7p.QX2QDO0wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@processes~resuming-processes:~$ /challenge/run
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with 
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg
/challenge/run
I'm back! Here's your flag:
pwn.college{s0XT2PneDuxhSUzVnHBbct6YF7p.QX2QDO0wiMwkjNzEzW}
Don't forget to press Enter to quit me!

Goodbye!
```

## Incorrect tangents I went on
None to report in this instance.

## What I learned
Upon suspension of a process, the terminal being regained allows for us to continue using it with the process paused indefinitely, to resume it, we use a builtin 'fg' which resumes suspended processes of the terminal.

## References
None to report here.