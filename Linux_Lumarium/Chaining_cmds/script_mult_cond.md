# Challenge name
Scripting with multiple conditions

## My solve
**Flag:** `pwn.college{4VuHi7_KhdoSpC-JNyFuUzCrLSW.0FOzMDOxwiMwkjNzEzW}`

```bash
hacker@chaining~scripting-with-multiple-conditions:~$ nano solve.sh 
hacker@chaining~scripting-with-multiple-conditions:~$ ./solve.sh hack
the planet
hacker@chaining~scripting-with-multiple-conditions:~$ /challenge/run
Correct! Your script properly handles all the conditions with elif.
Here's your flag:
pwn.college{4VuHi7_KhdoSpC-JNyFuUzCrLSW.0FOzMDOxwiMwkjNzEzW}
```

## Incorrect tangents I went on
None to note here

## What I learned
Here we are allowed to nest the if statement through the elif(else if) statement which checks for another condition if the initial if statement fails, instead of terminating the program. This allows for a variety of parameters to be checked and topically enacted on in accordance to their valididty allowing for the if condition to take form of many inputs and yeild accordingly variate output. 

## References
None.