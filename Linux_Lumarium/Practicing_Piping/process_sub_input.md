# Challenge Name
Process Substitution for Input.

## My solve
**Flag:** `pwn.college{kygqpi0UFMxOtj2aE8JL8qhoUSI.0lNwMDOxwiMwkjNzEzW}`

```bash
hacker@piping~process-substitution-for-input:~$ diff <(/challenge/print_decoys_and_flag) <(/challenge/print_decoys)
62d61
< pwn.college{kygqpi0UFMxOtj2aE8JL8qhoUSI.0lNwMDOxwiMwkjNzEzW}
```

## Incorrect tangents I went on
Here I has initially echoed the named pipes of the echo of the files. That did not carry any data and I could not diff the two files as they only containted nonexistent paths that did not yeild any directory or file. Eventually I diffed the input process subtitution of the two commands.

## What I learned
To increse productivity and efficiency of the program before dffing the file, we can hook input and output of programs to arguments of commands using process substitution, here was use input process substitution (<()) to hook the command's output into a temporary file aptly named as a "named pipe". In basic terms, it passes a command output as a file for reading. Note that we can call this process substitution multiple times in a go.

## References 
None here.
