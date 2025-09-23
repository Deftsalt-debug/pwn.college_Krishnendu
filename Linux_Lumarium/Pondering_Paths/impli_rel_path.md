# Challenge name
Implicit relative paths from /

## My solve
**Flag:** `pwn.college{Q-U7ISCDq8obbujQiY-mRX5sBXM.QX5QTN0wiMwkjNzEzW}`

```bash
Connected!
hacker@paths~implicit-relative-paths-from-:~$ /challenge/run
Incorrect...
You are not currently in the / directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ ../challenge/run
Incorrect...
This challenge must be invoked with a relative path that starts with a letter!
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{Q-U7ISCDq8obbujQiY-mRX5sBXM.QX5QTN0wiMwkjNzEzW}
```

## Incorrect tangents I went on
This was a case of me being far too stimulated with new information, using the parent directory ".." keyword when inside the root directory and instead pulling me from the root directory and trying to access nothing per se. All there is to do is cd into root directory and run challenge/run via relative pathing (as the hint said).

## What I learned
Relative pathing, as the name states, requires pathing to be done RELATIVE to our current directory. This is contrast to the previous challenges which relied on the fact that we invoked the absolute path irrespective to the current directory. Absolute paths are a lot more precice in the means to reach the file whereas relative paths are a lot easier to use but require a base anchor, central to which we navigate to a file (here we are accessing it from root)  

## References
None to be applicable