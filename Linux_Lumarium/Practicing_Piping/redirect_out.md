# Challenge name
Redirecting Output

## My solve
**Flag:** `pwn.college{UQi21ZtoS074p9huMBdZKL-_cRL.QX0YTN0wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your 
flag:
pwn.college{UQi21ZtoS074p9huMBdZKL-_cRL.QX0YTN0wiMwkjNzEzW}
```

## Incorrect tangents I went on
None to prompt here.

## What I learned
The '>' operator, as the challenge name states, redirects a specific output into a file. This output could be from a grep, cat or, as we did here, an echo. Here we echo the string "PWN" (just prints the argument passed, i.e PWN) suffixed by the > we reroute that output into the file COLLEGE. After passing this command, if we were to cat into COLLEGE, we'd get the string "PWN". 

## References
None to record here. 