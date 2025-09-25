# Challenge name 
Redirecting Errors

## My solve
**Flag:** `pwn.college{wuVlyVF4qU_d8QoolQDKtiyL5bY.QX3YTN0wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2>instructions
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{wuVlyVF4qU_d8QoolQDKtiyL5bY.QX3YTN0wiMwkjNzEzW}
```

## Incorrect tangents I went on
None to report on this front.

## What I learned
This was an intuitive learn of using file discriptors, numbers which are usually used to descibe the type of prompt given by us or the shell. 0, being of general input; 1, as standard output and 2 as errors. The rerouting/redirection of a process' communication is implicity done by the '>' command, being equivalent to prefixing the 1 file descriptor to it (i.e. '1>'). The prefixing of the 2 FD gives a reroute of the process's errors into the file (2>) and as this challenge dictates, we are totally able to use multiple file descriptors and rerouting at the same time, here we reroute /challenge/run's output into myflag and it's error into instructions using file descriptors for the error but not for the output as it is implicit and equivalent to not prefixing anything. 

## References 
None to note here.