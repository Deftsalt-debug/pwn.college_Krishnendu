# Challenge Name
Grepping live output

## My solve
**Flag:** `pwn.college{A9yPQP2-Ke91pfUcDhPZ8L4KI4b.QX5EDO0wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@piping~grepping-live-output:~$ /challenge/run | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stdout : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stdout!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{A9yPQP2-Ke91pfUcDhPZ8L4KI4b.QX5EDO0wiMwkjNzEzW}
```

## Incorrect tangents I went on
None to write about here

## What I learned
It's incremental to ask after the previous challenges if we can pass outputs of commands directly as intputs into other commands without the use of any file and the answer is a resolute yes. We see that through the piping operator | we are able to exclude the usage of files in the rerouting of inputs and outputs to different commands alone into each other. Output from the command to the left of the pipe will be rerouted the standard input of the command to the right of the pipe.

## References
None to note here. 