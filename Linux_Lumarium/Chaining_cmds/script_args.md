# Challenge name
Scripting with arguments

## My solve
**Flag:** `pwn.college{89xZ2JcREfXbSE0-vNfXBcBhqNf.0VNzMDOxwiMwkjNzEzW}`

```bash
hacker@chaining~scripting-with-arguments:~$ nano solve.sh
hacker@chaining~scripting-with-arguments:~$ ./solve.sh pwn college
college pwn
hacker@chaining~scripting-with-arguments:~$ /challenge/run
Correct! Your script properly reversed the arguments.
Here's your flag:
pwn.college{89xZ2JcREfXbSE0-vNfXBcBhqNf.0VNzMDOxwiMwkjNzEzW}
```

## Incorrect tangents I went on 
None to note here

## What I learned
Scripting can add another layer of interactivity by allowing us to take in extra arguments to a general script. This is achieved using a set of special variables ($1, $2 and so on) which represent the arguments passed as variables into the script.
 
## References
None to note here.