# Challenge name
Starting Background Processes

## My solve
**Flag:** `pwn.college{IPgedsj5VEfGN2FdFNZ0pVz7enw.QX5QDO0wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@processes~starting-backgrounded-processes:~$ /challenge/run &
[1] 139
hacker@processes~starting-backgrounded-processes:~$ 


Yay, you started me in the background! Because of that, this text will probably 
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{IPgedsj5VEfGN2FdFNZ0pVz7enw.QX5QDO0wiMwkjNzEzW}
```

## Incorrect tangents I went on 
None to note here.

## What I learned
To run a process in a background without initially suspending the process, we can suffix a & to the process call. This explicitly runs the process in the background. 

## References
None here.