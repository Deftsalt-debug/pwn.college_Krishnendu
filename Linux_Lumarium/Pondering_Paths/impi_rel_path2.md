# Challenge name
Implicit Relative Path

## My solve
**Flag:** `pwn.college{og3TbSRPSgCIgU60YbFAkMX5p8R.QXxUTN0wiMwkjNzEzW}`

```bash
Connected!
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{og3TbSRPSgCIgU60YbFAkMX5p8R.QXxUTN0wiMwkjNzEzW}
```

## Incorrect Tangents I went on
None to record here

## What I learned
This was an extremely satisfying challenge, culminating with us utilising explicit relative paths to invoke the file. We are using the '.' entry to the relative paths so as to counter linux's failsafe which is triggered when we send a naked relative path which yeilds the error `bash: run: command not found`. The action of actually, explicitly, signifying our pathing gives us as the user as well as the system that we actually *want* to access the file instead of running something or confuse any interpretation of the command we sent. Note that in previous challenges I was messing up due to my use of this form of pathing regularly instead of calling the desired "naked" path then.

## References
None here
