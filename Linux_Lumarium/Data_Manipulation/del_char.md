# Challenge name
Deleting characters

## My solve
**Flag:** `pwn.college{chS_RHyBpy3wVdntxohd3P839xk.0FNxEzNxwiMwkjNzEzW}`

```bash
hacker@data~deleting-characters:~$ /challenge/run | tr -d %^
Your character-stuffed flag:
pwn.college{chS_RHyBpy3wVdntxohd3P839xk.0FNxEzNxwiMwkjNzEzW}
```

## Incorrect tangents I went on 
None to note here

## What I learned
Building off of the previous module discussing the tr command, we now learn a a flag that can be passed to tr to now delete characters -d; instead of modifying and translating them, we're now gonna have tr delete the characters from the stdout of the command that's piped into it. 

## References
None to report here.