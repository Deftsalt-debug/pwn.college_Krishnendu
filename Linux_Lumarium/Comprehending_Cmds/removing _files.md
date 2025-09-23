# Challenge name
Removing Files

## My solve
**Flag:** `pwn.college{EJ9A3Vi20Nzb3wJkjh6sFrbkT2g.QX2kDM1wiMwkjNzEzW}`

```bash
Connected!
hacker@commands~removing-files:~$ ls
Desktop  a  delete_me
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{EJ9A3Vi20Nzb3wJkjh6sFrbkT2g.QX2kDM1wiMwkjNzEzW}
```

## Incorrect tangents I went on
Nothing here

## What I learned
'rm' is another key tool to navigating the command line and our system, to remove files we will need to pass the filename as an argument while being under the directory containing the file. Here we call rm with the file 'delete_me' and it subseqently deletes it from the system.

## References
None