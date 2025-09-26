# Challenge name
Grepping Errors 

## My solve
**Flag:** `pwn.college{snPNx6yVFvqZLqFicSVCBsJOMmZ.QX1ATO0wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@piping~grepping-errors:~$ /challenge/run 2>& 1| grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stderr : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stderr to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{snPNx6yVFvqZLqFicSVCBsJOMmZ.QX1ATO0wiMwkjNzEzW}
```

## Incorrect tangents I went on
None to report here

## What I learned
The default nature of the pipe operator forbids the use of anything to be passed into it that isn't a standard output. So if we were to pipe an error, we'd need an equivalent to a file descriptor but for commands since FD operator(>) are only exclusive to files. Thankfully the shell includes the '>&' operator, which redirects a file descriptor to another file descriptor, so therefore we can reroute the error using the 2 FD and the >& operator into 1 FD and pipe the error masked as FD 1 (standard output) into the pipe without any error and pipe it into grep for searching the flag.

## References
None to note here.
