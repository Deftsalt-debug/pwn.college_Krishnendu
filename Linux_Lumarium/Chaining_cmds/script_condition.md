# Challenge name
Scripting with conditionals

## My solve
**Flag:** `pwn.college{s-ILdqM6h7hlOL3GI0_daBP-LWB.0lNzMDOxwiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@chaining~scripting-with-conditionals:~$ nano solve.sh
hacker@chaining~scripting-with-conditionals:~$ ./solve.sh 
./solve.sh: line 2: [: missing `]'
hacker@chaining~scripting-with-conditionals:~$ nano solve.sh 
hacker@chaining~scripting-with-conditionals:~$ ./solve.sh 
hacker@chaining~scripting-with-conditionals:~$ ./solve.sh pwn
college
hacker@chaining~scripting-with-conditionals:~$ /challenge/run
Correct! Your script properly handles all the conditions.
Here's your flag:
pwn.college{s-ILdqM6h7hlOL3GI0_daBP-LWB.0lNzMDOxwiMwkjNzEzW}
```

## Incorrect tangents I went on
Here I had placed the conditonal statement under if without any spaces, causing the script to fail. This was due to a muscle memory with other languages where leaving a space between the statement and the parantheses was not an issue.

## What I learned
The if command allows for conditionallity in arguments passed into the script. Allowing for contextual decisions and commands to be executed in accordance to specific arguments. There must be spaces after the parantheses and the statements cannot be compressed into a single line, they must have seperators such as a semicolon or being written on difference lines. They must also terminate with a fi to close the conditionality. 

## References
None to note here.