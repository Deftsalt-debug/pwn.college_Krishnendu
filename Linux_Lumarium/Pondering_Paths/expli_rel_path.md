# Challenge Name
Explicit relative paths from /

## My solve
**Flag:** `pwn.college{YFaAwKQz0Tk70MKxUrHBKTbCXve.QXwUTN0wiMwkjNzEzW}`

```bash
Connected!
hacker@paths~explicit-relative-paths-from-:~$ /challenge/run
Incorrect...
You are not currently in the / directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{YFaAwKQz0Tk70MKxUrHBKTbCXve.QXwUTN0wiMwkjNzEzW}
```

## Incorrect tangents I went on 
None to record here

## What I learned
This was a statisfying one, if you observe my previous workings to challenges, I was attempting explicit pathing in situations where it wasn't supposed to be used. Here we are using the '.' operator/entry to our relative path esentially telling us to look into the root (/) directory and access challenge from there itself. As stated in the pwn.college website, these entries give us more legibiliy to our statements and clothe our relative paths which were previously 'naked' 

## References
None here