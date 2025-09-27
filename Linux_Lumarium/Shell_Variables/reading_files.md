# Challenge name
Reading files

## My solve
**Flag:** `pwn.college{Yujq608cVJhCRmLsVoAhG2zDB8P.QXwIDO0wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@variables~reading-files:~$ read PWN < (/challenge/read_me)
bash: syntax error near unexpected token `('
hacker@variables~reading-files:~$ read PWN < /challenge/read_me
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{Yujq608cVJhCRmLsVoAhG2zDB8P.QXwIDO0wiMwkjNzEzW}
```

## Incorrect tangents I went on
Out of sheer force-of-habit, I had accidently placed the /read-me command under brackets which did not follow syntax. This was didn't even do a process subtitution as there was a whitespace between the < and parentheses.

## What I learned
A more efficient manner to read a command into an environmental variable, without the use and cat of a pointless file can be achieved through the use of read. Rerouting of input into read can assign its value without the use of any file or catting to occur. We here redirect the output of /challenge/read-me as stdin of read which assigns the output of /read-me into PWN. 

## References
None here.