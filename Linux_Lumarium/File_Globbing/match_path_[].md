# Challenge name
Matching paths with [] 

## My solve
**Flag:** `pwn.college{cERFYXk_KwsbuBq-xR4H-UbZ8MK.QX0IDO0wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{cERFYXk_KwsbuBq-xR4H-UbZ8MK.QX0IDO0wiMwkjNzEzW}
```

## Incorrect tangents I went on
Here I had initially pre-globbed by not passing the path of the file_[bash] instead only passing /challenge/files followed by file_[bash] which wasn't accessing anything to glob. There was also in instance where I considered cd'ing into /challenge/files and running the command from there.

## What I learned
Paths too can be globbed by [], we can specify a set list of files by globbing them as a path altogether and allowing us to expand entire sets of paths through it. 

## References
None to record. 