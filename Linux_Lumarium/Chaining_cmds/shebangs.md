# Challenge name
Understanding shebangs

## My solve
**Flag:** `pwn.college{UvWy8G1ivWlPWw1OoSJm6WyFk6p.0VOzMDOxwiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@chaining~understanding-shebangs:~$ nano solve.sh
hacker@chaining~understanding-shebangs:~$ chmod a+x solve.sh
hacker@chaining~understanding-shebangs:~$ /challenge/run
Testing your script...
Perfect! Your flag:
Flag: pwn.college{UvWy8G1ivWlPWw1OoSJm6WyFk6p.0VOzMDOxwiMwkjNzEzW}
```

## Incorrect tangents I went on
None to note here


## What I learned
The linux shell determines shell script not based on its file extension but moreso the shell looks into the first few bytes of the program to understand its significance. Here we look into a specific type of file we've been using for our shell scripts that being of an interpreted program. If the program file starts with the a shebang(consisting of #), Linux treats the file as so and passes the file to the shell interpreter as its only argument thus executing the script. The shell here automatically reads off of the first line of the script at the shebang and calls the bash command implicitly. #!/bin/bash is for bash scripts and #!/usr/bin/python3 is for Python scripts.

## References
None to note here.