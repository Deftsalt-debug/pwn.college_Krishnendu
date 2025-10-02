# Challenge name
Detaching and Attaching

## My solve
**Flag:** `pwn.college{wpITvWz88Y-gwpdMGa6sonYDWZS.0lN4IDOxwiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@terminal-multiplexing~detaching-and-attaching:~$ screen
[detached from 140.pts-0.terminal-multiplexing~detaching-and-attaching]
hacker@terminal-multiplexing~detaching-and-attaching:~$ screen -r
[detached from 140.pts-0.terminal-multiplexing~detaching-and-attaching]
hacker@terminal-multiplexing~detaching-and-attaching:~$ /challenge/run
Found detached screen session: 140.pts-0.terminal-multiplexing~detaching-and-attaching
Sending flag to your screen session...

Flag sent! Now reattach to your screen session with:

  screen -r

You'll find the flag waiting for you there!
hacker@terminal-multiplexing~detaching-and-attaching:~$ screen -r
[screen is terminating]

hacker@terminal-multiplexing~detaching-and-attaching:~$
hacker@terminal-multiplexing~detaching-and-attaching:~$ echo Yes! Flag is: pwn.college{wpITvWz88Y-gwpdMGa6sonYDWZS.0lN4IDOxwiMwkjNzEzW}
```

## Incorrect tangents I went on
None to note here

## What I learned
We can detach and reattach windows into our shell allowing for a seamless workflow in getting to a specific process and moving to another. Attaching means connecting to a running shell with its own processes, while detaching means disconnecting from it without terminating. Detaching is done by Ctrl+A followed by d and reattaching to the same screen is done by the same screen command now passed with a -r argument/flag. Ctrl A is also screen's activation key for all its shortcuts. 

## References
None.