# Challenge name
Duplicating piped data using tee

## My solve
**Flag:** `pwn.college{wzbA-znycLvshCU5yRMUUd5YMQB.QXxITO0wiMwkjNzEzW}`

```bash 
Connected!                                                                        
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | /challenge/college
Processing...
The input to 'college' does not contain the correct secret code! This code 
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the 
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee pwn | /challenge/college
Processing...
The input to 'college' does not contain the correct secret code! This code 
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the 
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat pwn
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "wzbA-zny"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret wzbA-zny | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{wzbA-znycLvshCU5yRMUUd5YMQB.QXxITO0wiMwkjNzEzW}
```

## Incorrect tangents I went on
Here I had initially used tee into /challenge/college which yeilded an error and sent me into a very ridiculous error where I omitted tee itself out of sheer curiosity. Both yeilding in error and making me redirect /challenge/pwn into the file pwn and /challenge/college via the tee command.

## What I learned
The tee command is a method by which we reroute the output to be piped into two different destinations, by essence splitting the piping and creating a junction from which the output is passed into two different destinations (this is like piping two times at once). Thus creating two copies of the output from /challenge/pwn, one into the file pwn and into the /challenge/college. Catting pwn gives us the exact argument we need to pass to get the flag and we repipe the /challenge/pwn into /challenge/college with the correct argument to obtain the flag

## References 
None here.