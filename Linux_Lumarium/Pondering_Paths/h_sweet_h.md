# Challenge name
Home Sweet Home

## My solve
**Flag:** `pwn.college{kducxgcOGvIvC55WEtCJ0jokNDJ.QXzMDO0wiMwkjNzEzW}`

```bash
Connected!
hacker@paths~home-sweet-home:~$ /challenge/run/abc
bash: /challenge/run/abc: Not a directory
hacker@paths~home-sweet-home:~$ /challenge/run ~/abc
The argument you provided must not have been longer than 3 characters (it's
currently 5 characters long)!
hacker@paths~home-sweet-home:~$ /challenge/run ~/a
Writing the file to /home/hacker/a!
... and reading it back to you:
pwn.college{kducxgcOGvIvC55WEtCJ0jokNDJ.QXzMDO0wiMwkjNzEzW}
```

## Incorrect tangents I went on
As we can see in the above segment, I have assumed our file was going to somehow automatically augment and magically appear if we called it via it's absolute path. This was not the way to go and was a very silly mistake. The subsequent error was even more blasphemous as we see that despite me being on the right path by invoking the /challenge/run followed by the file abc under the home directory, I failed to consider that '~/' are included in the character limit of 3 characters. After this embarassment I quickly course-corrected. 

## What I learned
The home directory is shorthanded by the character '~', in the pwn.college environment, this would be /home/hacker. Despite being a shorthand notation, '~' is an absolute path which we can call, as we did in this challenge. We also subsequently learnt that passing cd without any relative paths or arguments by default would send us down to our home directory. The challenge incorporated a simple yet intuitive manner by which we invoked /challenge/run under a set absolute path under contraints, achieved by the ~ prompt.

## References
None to note here.