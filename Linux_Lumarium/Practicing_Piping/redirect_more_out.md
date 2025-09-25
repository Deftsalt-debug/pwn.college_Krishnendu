# Challenge name
Redirecting more output

## My solve
**Flag:** `pwn.college{05aZIACsJRIbxPfpQlSFjK1_ufH.QX1YTN0wiMwkjNzEzW}`

```bash 
Connected!                                                                        
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{05aZIACsJRIbxPfpQlSFjK1_ufH.QX1YTN0wiMwkjNzEzW}
```

## Incorrect tangents I went on
None to report here

## What I learned
This is iterative off of the previous challenge, here we redirect the output of /challenge/run (which gives us our flag) into the file myflag. After which we cat into myflag and obtain the resultant flag required. This module gives us confirmation that the rerouting of outputs works for commands too.

## References
None to note here. 