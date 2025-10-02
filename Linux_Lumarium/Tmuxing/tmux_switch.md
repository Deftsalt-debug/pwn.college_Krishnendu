# Challenge name
Switching Windows (tmux) 

## My solve
**Flag:** `pwn.college{gw695Wq4YiMGSoSDxC1wLeL87R5.0FM5IDOxwiMwkjNzEzW}`

```bash 
hacker@terminal-multiplexing~switching-windows-tmux:~$ tmux
[exited]
hacker@terminal-multiplexing~switching-windows-tmux:~$ tmux a
[detached (from session challenge_session)]

hacker@terminal-multiplexing~switching-windows-tmux:~$  cat <<MSG
> Excellent work! You found window 0!
> Here is your flag: pwn.college{gw695Wq4YiMGSoSDxC1wLeL87R5.0FM5IDOxwiMwkjNzEzW}
```

## Incorrect tangents I went on
Here I had accedentally created a new instance of tmux instead of reattaching into the challenge's window, thus having to pass 'a' as the argument to tmux so as to reattach to the window.

## What I learned
Tmux allows for a few commands similar in vein to screen but obviously now with a different command prefix(ctrl-b). We attach a key character with the command prefix to allow for numerous processes in tmux such as creating windows(c), switching between them(0-9), picking a window(w) or sikmming past the next and previous windows(n, p). 

## References
None.
