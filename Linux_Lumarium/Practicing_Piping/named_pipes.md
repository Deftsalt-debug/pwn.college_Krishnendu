# Challenge name 
Named Pipes

## My solve
**Flag:** `pwn.college{gGzu8i_RIoF1scY3bSR1OOQ28PL.01MzMDOxwiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@piping~named-pipes:~$ mkfifo /tmp/flag_fifo
hacker@piping~named-pipes:~$ /challenge/run > /tmp/flag_fifo
You're successfully redirecting /challenge/run to a FIFO at /tmp/flag_fifo! 
Bash will now try to open the FIFO for writing, to pass it as the stdout of 
/challenge/run. Recall that operations on FIFOs will *block* until both the 
read side and the write side is open, so /challenge/run will not actually be 
launched until you start reading from the FIFO!

Connected!
hacker@piping~named-pipes:~$ cat /tmp/flag_fifo
You've correctly redirected /challenge/run's stdout to a FIFO at 
/tmp/flag_fifo! Here is your flag:
pwn.college{gGzu8i_RIoF1scY3bSR1OOQ28PL.01MzMDOxwiMwkjNzEzW}
```

## Incorrect tangents I went on
None to note here

## What I learned
This challenge teaches us to create named, persistent pipes, called FIFO's, they follow a similar principal to the queue datastructure in this regard and are created using the mkfifo command. FIFO's can be controlled by specifing its path and persist until we delete them. As we see though, the pipe requires to have both read and write portions are open and it's connections *set*. Here if any end is "blocked", the operation is hanged until the prequisite of reading/writing is fulfilled here.  

## Refereneces
None to place here.