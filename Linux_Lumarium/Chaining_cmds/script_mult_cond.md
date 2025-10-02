# Challenge name
Scripting with multiple conditions

## My solve
**Flag:** `pwn.college{IFOxSr4K-mPLEpToCRk0WpfQ96l.01NzMDOxwiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@chaining~scripting-with-default-cases:~$ nano solve.sh 
hacker@chaining~scripting-with-default-cases:~$ ./solve.sh 
nope
hacker@chaining~scripting-with-default-cases:~$ /challenge/run
Correct! Your script properly handles the if/else conditions.
Here's your flag:
pwn.college{IFOxSr4K-mPLEpToCRk0WpfQ96l.01NzMDOxwiMwkjNzEzW}
```

## Incorrect tangents I went on
None to note here, I had just initially forgot to close the nope string with quotes under solve.sh.

## What I learned
We can stack arguments into complex structures under the conditional statements. This is further achieved by the else statement which is actuated if none of the parameters of the if statement is satisfied and allows for another layer of conditionality and a manner to end the conditional statement as a failsafe. This further expands on conditional statements in a broad sense.

## References
None.