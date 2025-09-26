# Challenge name
Split-piping stderr and stdout

## My solve
**Flag:** `pwn.college{8OIJuJgRjil6k3JgWFfqvbni7FB.QXxQDM2wiMwkjNzEzW}`

```bash
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack > >(/challenge/planet) 2> >(/challenge/the)
Congratulations, you have learned a redirection technique that even experts 
struggle with! Here is your flag:
pwn.college{8OIJuJgRjil6k3JgWFfqvbni7FB.QXxQDM2wiMwkjNzEzW}
```

## Incorrect tangents I went on 
I had initially tried to redirect using tee which just took the stdout of /hack into both the files failing to satisfy the condition stated by the program. Tee simply writes to a file at /path whereas > >(/path) connects stdout into the program's stdin while running /path as a *command*. I had then mistakenly tried to pipe stdout of the /planet via process subtitution into /the which was pointless and menial. Eventualy I looked over the reference websites. Stackedoverflow which gave me a solution using subshells and brace groups which were way beyond my comprehension right now. 

## What I learned
Here we use write-substitutions along with file descriptors to state the purpose of what we expect off of /hack. We pipe /hack's stdout and stderr into two arguments, one substitution sending stdout of /hack as stdin of /planet, the next one, with an explicit fd of stderr redirects the stderr of /hack as a stdin of /the. Thus satisfying the problem. Note that the shell replaces the >(...) expression with the path to the pipe. 

## References 
https://web.archive.org/web/20220629044814/http://bencane.com:80/2012/04/16/unix-shell-the-art-of-io-redirection/