# Challenge name
The PATH Variable

## My solve
**Flag:** `pwn.college{QyYJu8hIluZGPeppN43V0JIKus1.QX2cDM1wiMwkjNzEzW}`

```bash
hacker@path~the-path-variable:~$ export PATH=""
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
pwn.college{QyYJu8hIluZGPeppN43V0JIKus1.QX2cDM1wiMwkjNzEzW}
```

## Incorrect tangents I went on
None to write about for the time being.

## What I learned
The PATH variable is a unique variable created by the shell to store directory paths from which the shell will search for programs in response to commands interpreted by it. This variable though, can be modified and if blanked out would lead to numerous commands requiring a directory path to fail entirely such as ls and rm. 

## References
None to report on this front.
