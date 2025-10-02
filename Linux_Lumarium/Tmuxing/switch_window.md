# Challenge name
Switching Windows.

## My solve
**Flag:** `pwn.college{Is72sc-SKgxaFcoBMLN9IpKnrcl.0FO4IDOxwiMwkjNzEzW}`

```bash 
hacker@terminal-multiplexing~switching-windows:~$ screen -r
^A 0
hacker@terminal-multiplexing~switching-windows:~$  cat <<MSG
> Excellent work! You found window 0!
> Here is your flag: pwn.college{Is72sc-SKgxaFcoBMLN9IpKnrcl.0FO4IDOxwiMwkjNzEzW}
```

## Incorrect tangents I went on
None to report here.

## What I learned
The screen serves as an exellent means to multitask and switch between processes. When inside a screen we can create further shells called windows, between which we can switch using ctrl+a along with a key character which can swap between numbered windows (0-9), list them (") or create a new one (c). We can think of these windows belonging to the same shell but each being allowed to work on whatever the user intends for them to (here we use the example of tabs in a browser). 

## References
None to note here.