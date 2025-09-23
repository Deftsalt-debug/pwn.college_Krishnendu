# Challenge name
Listing Files

## My solve
**Flag:** `pwn.college{Q6M-xUN4tpb6OWb22T-Xw5_yrkF.QX4IDO0wiMwkjNzEzW}`

```bash
Connected!
hacker@commands~listing-files:~$ ls /challenge
27458-renamed-run-20682  DESCRIPTION.md
hacker@commands~listing-files:~$ /challenge/27458-renamed-run-20682
Yahaha, you found me! Here is your flag:
pwn.college{Q6M-xUN4tpb6OWb22T-Xw5_yrkF.QX4IDO0wiMwkjNzEzW}
```

## Incorrect Tangents I went on
None to note here

## What I learned
The 'ls' command is an essential to say the least, the challenge here has presented a situation where /challenge/run has been renamed. Here 'ls' is used to *list* the files under the passed directory, we can pass a specific directories' path as an argument whose contents we want to know. If ls is passed without an argument it would simply list the contents of the current directory we are in.  

## References
None to note here