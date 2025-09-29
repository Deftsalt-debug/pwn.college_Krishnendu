# Challenge name
Deleting newlines

## My solve
**Flag:** `pwn.college{ICWQmFDv7I3GRZLuN3mBzG1-LP_.0VNxEzNxwiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@data~deleting-newlines:~$ /challenge/run | tr -d "\n"
Your line-split flag: pwn.college{ICWQmFDv7I3GRZLuN3mBzG1-LP_.0VNxEzNxwiMwkjNzEzW}
```

## Incorrect tangents I went on
None for the time being.

## What I learned
The insertion of newline is characterised through the escape sequence \ followed by the character n, It has to be specified under quotes to allows the shell interpreter to understand that there is a new line to jump the cursor into during output instead of actually *interpreting* the sequence. Note that if we want to represent the forward slash as an acutal character instead of an escape sequence, we have to use the slash twice '//' allowing for the shell and tr to use the actual forward-slash character. 

## References
None here.