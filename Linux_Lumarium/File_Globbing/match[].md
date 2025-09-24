# Challenge name
Matching with []

## My solve
**Flag:** `pwn.college{0kvenSAhc7dFy5hcEB4Tg09NJAj.QXzIDO0wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{0kvenSAhc7dFy5hcEB4Tg09NJAj.QXzIDO0wiMwkjNzEzW}
```

## Incorrect tangents I went on
Here, I accidentally misinputted file_[bash] into the path, yeilding an error as that file or directory does not exist under /challenge/run. Thus requiring the argument to be attached seperately to the path. 

## What I learned
Globbing with [] is basically further bootstrapping ? by limiting the search set for the character to be autofilled/wildcarded in the argument to whatever characters are present *inside* the brackets. 

## References
None to note here.