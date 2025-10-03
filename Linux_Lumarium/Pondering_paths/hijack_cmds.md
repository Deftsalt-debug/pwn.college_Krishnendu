# Challenge name
Hijacking Commands

## My solve
**Flag:** `pwn.college{o7nCjwas8mz7id0B1WnB5Rzx8B_.QX3cjM1wiMwkjNzEzW}`

```bash
hacker@path~hijacking-commands:~$ nano rm
hacker@path~hijacking-commands:~$ chmod a+x ~/rm
hacker@path~hijacking-commands:~$ PATH=~
hacker@path~hijacking-commands:~$ /challenge/run 
Trying to remove /flag...
pwn.college{o7nCjwas8mz7id0B1WnB5Rzx8B_.QX3cjM1wiMwkjNzEzW}
```

## Incorrect tangents I went on
Here I initially tried to simply overwrite and clear PATH and try to externally cat (via path) the /flag. This didn't work as I failed to consider that /challenge/run didn't print anything and catting /flag is not permitted (literally cheating lol)

## What I learned
Here we modify a specific command to do an entirely different task as it was prescribed to do. This instance calls for us to modify a script named rm exactly as the command and flip it to actually print /flag. We then make it an executable via chmod and then overwrite PATH thus removing the path to the *ACTUAL* rm command (which removes files) and making /challenge/run actually print the file (thinking it's used rm) as we've now only placed PATH to subtitute bare calls of rm to print /flag. 

## References
None.