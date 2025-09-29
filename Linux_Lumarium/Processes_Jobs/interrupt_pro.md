# Challenge name
Interrupting Processes

## My solve
**Flag:** `pwn.college{ogTxww8DVw5fkvl31QI1M1aFAcZ.QXzQDO0wiMwkjNzEzW}`

```bash
hacker@processes~interrupting-processes:~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember, 
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{ogTxww8DVw5fkvl31QI1M1aFAcZ.QXzQDO0wiMwkjNzEzW}
```

## Incorrect tangents I went on
On mac, the control button is usually rerouted to the command button, this did not work in this instance, I soon tried control+option+c which was the key to making the program interrupt.

## What I learned
Ctrl+C is a hotkey to *interrupt* a shell command to a process requring our input from the terminal end. It is a cleaner and quicker way to stop a process instead of killing it. 

## References
None here.