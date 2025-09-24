# Challenge name
Help for builtins

## My solve 
**Flag:** `pwn.college{YWQe8dUpJmyHLzIrGBes_dxhOd-.QX0ETO0wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!
    
    Options:
      --fortune		display a fortune
      --version		display the version
      --secret VALUE	prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "YWQe8dUp".
hacker@man~help-for-builtins:~$ challenge --secret YWQe8dUp
Correct! Here is your flag!
pwn.college{YWQe8dUpJmyHLzIrGBes_dxhOd-.QX0ETO0wiMwkjNzEzW}
```

## Incorrect tangents I went on
None to record 

## What I learned
In commands such as cd, there is no such thing as a --help argument or any manpages. Here, these commands are built into the shell (hence, builtins). The shell handles the commands internally and the help keyword followed by the builtin as an argument gives us a shell generated prompt on vital information about the builtin. Serving the same purpose as the documentation and --help did.

## References
None to add here.