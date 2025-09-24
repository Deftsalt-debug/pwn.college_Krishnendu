# Challenge name
Multiple Globs

## My solve
**Flag:** `pwn.college{IqApJZtNjp3ZFfX97Ty4LbQLQ3S.0lM3kjNxwiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@globbing~multiple-globs:~$ cd /challenge/files
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{IqApJZtNjp3ZFfX97Ty4LbQLQ3S.0lM3kjNxwiMwkjNzEzW}
```

## Incorrect tangents I went on
Here I had intitally passed the argument 'p** ' which did not assume that the file *couldn't* start with a p too. All the question told us is that the filename, of unknown length, contains a p in there. Thus the more sensible approach would be to pass the argument as *p* compensating for both cases where there is wildcards before and after p. 

## What I learned
Bash and the command shell allows for the implementation of multiple globs into an argument. The shell essentially can run all permuations of the wildcard(s) to check for matches to the argument, including the instance where the glob(s) would contain nothing. This allows for an even more abstract argument to be passed to the shell and still yeild a correct set from the system depending on the accuracy of how many known characters are passed as the argument. 

## References
None to place. 