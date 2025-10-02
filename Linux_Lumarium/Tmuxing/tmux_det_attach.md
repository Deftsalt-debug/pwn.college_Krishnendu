# Challenge name
Detaching and Reattaching(tmux)

## My solve
**Flag:** `pwn.college{clrH-XU6EYg6qwmwTF0CaI80DKK.0VO4IDOxwiMwkjNzEzW}`

```bash
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux
[detached (from session 0)]
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ /challenge/run
Found detached tmux session: 0
Sending flag to your tmux session...

Flag sent! Now reattach to your tmux session with:
  tmux attach

You'll find the flag waiting for you there!
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux a
[exited]
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$  echo Congratulations, here is your flag: pwn.college{clrH-XU6EYg6qwmwTF0CaI80DKK.0VO4IDOxwiMwkjNzEzW}
Congratulations, here is your flag: pwn.college{clrH-XU6EYg6qwmwTF0CaI80DKK.0VO4IDOxwiMwkjNzEzW}
```

## Incorrect tangents I went on
None to note here.

## What I learned
Tmux is a more modern and simple terminal multiplexer, it offers an added benefit of allowing window splitting and tiling of shells compared to the older screens. Tmux has its command prefix as ctrl+b instead of screen's ctrl-a, to detach from tmux we have to use the command prefix and d. To reattach we can just pass attach or just 'a' to tmux as an argument. Tmux ls also lists the available shells. 

## References
None to note here.