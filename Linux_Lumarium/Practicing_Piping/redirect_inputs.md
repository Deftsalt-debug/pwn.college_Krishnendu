# Challenge name
Redirecting Inputs

## My solve 
**Flag:** `pwn.college{g2lexUL5WY2Q-AuVD3Qe0Tri8eQ.QXwcTN0wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read 
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{g2lexUL5WY2Q-AuVD3Qe0Tri8eQ.QXwcTN0wiMwkjNzEzW}
```

## Incorrect tangents I went on
None to record here

## What I learned
Being akin to redirecting outputs, we now learn about redirection of inputs in the same vein which follow the same order and syntax but now only take the symbol '<' Here we redirect an echo of COLLEGE into PWN and pass that as an input into /challenge/run. Note that the '<' will be a right to left assignment. The FD(file descriptiors) of inputs would be equal to 0.

## References
None to report here.