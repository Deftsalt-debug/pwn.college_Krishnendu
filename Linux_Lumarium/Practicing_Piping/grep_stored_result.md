# Challenge name
Grepping Stored Results. 

## My solve
**Flag:** `pwn.college{oJ5Czr6c3dn1p7slbthv7EJNuHA.QX4EDO0wiMwkjNzEzW}`

```bash
hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /tmp/data.txt
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to a file called /tmp/data.txt. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~grepping-stored-results:~$ grep flag /tmp/data.txt
[FLAG] Here is your flag:
persiflage's
flagellates
flagrantly
flagon
flagellating
flagpole's
flagstones
flagstone's
flagstone
conflagrations
flagship
unflagging
flagged
persiflage
flag's
flagellums
flagellation's
flag
camouflage's
conflagration's
flagging
camouflages
flagstaff's
conflagration
camouflaging
flagon's
flagons
flagstaffs
camouflaged
flagships
flagpole
flagellated
flags
flagella
flagship's
flagellum's
flagellate
flagellation
flagpoles
flagstaff
flagellum
camouflage
flagrant
hacker@piping~grepping-stored-results:~$ grep pwn.college /tmp/data.txt
pwn.college{oJ5Czr6c3dn1p7slbthv7EJNuHA.QX4EDO0wiMwkjNzEzW}
```

## Incorrect tangents I went on
This was one of those errors you don't ofen think much about because you assume you are in the correct thought-process. Here I assumed the flag would be in a string such as "flag:..." without it occuring that all the flags up until now can be found without any fuss by simply grepping the string "pwn.college". Honestly ridiculous from my end. 

## What I learned
After the redirection of a prompt's output into a file, the question now arises about how we would exactly find a specific string in a hypothetical collection of thousands of outputs under the file. Here a nifty command we learnt in previous challenges is used called grep, which takes in two arguments and can search for a specific string under a file path and ending up outputting the exact full string in the file. Here we use it to find the flag (starts with "pwn.colege") under the file /tmp/data.txt. 

## References
None to place here.