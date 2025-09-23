# Challenge name
Moving files

## My solve
**Flag:** `pwn.college{oxmUPTCBriyBMWTsfCHxO-J6Nmx.0VOxEzNxwiMwkjNzEzW}`

```bash
Connected!
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{oxmUPTCBriyBMWTsfCHxO-J6Nmx.0VOxEzNxwiMwkjNzEzW}
```

## Incorrect tangents I went on
Due to an acute mis-read of the question I had originally cd'ed into /tmp and tried to invoke mv of /hack-the-planet into /flag, essentially doing the question the other way, I quickly realised my error and did it the other way through the home directory. cding too was seemingly pointless in retrospect. 

## What I learned
'mv' performs a movment of a file from on directory to another (could also be in the same directory) wherein we pass two arguments into the command, the file where we want to source from and the file which will be its destination. It can be used to rename files, relocate them, as well as the renaming of directories. Here we move /flag into /tmp/hack-the-planet. 

## References
None to note here