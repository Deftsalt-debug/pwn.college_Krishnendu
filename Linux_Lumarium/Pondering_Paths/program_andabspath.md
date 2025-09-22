# Challenge name
Program and absolute paths

## My solve
**Flag:** `pwn.college{IQVbuzz8G8YTKmjh48eY0sseb2J.QX1QTN0wiMwkjNzEzW}`

```bash
Connected!
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{IQVbuzz8G8YTKmjh48eY0sseb2J.QX1QTN0wiMwkjNzEzW}
```

## Incorrect tangents I was on
None here, all good

## What I learned
This further adds another layer of complexity with a sub-directory containing the program, all of which is attached to the root directory, which we access by writing the full absolute path of the file instead of individually navigating the computer directories using 'cd'. The absolute path here is derivative of the previous challenge utilising the root directory to execute the program. 

## References
None to note