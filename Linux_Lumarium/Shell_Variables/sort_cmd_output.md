# Challenge name 
Storing Command Output

## My solve
**Flag:** `pwn.college{MvOzHgjuea5aAzWbBVWCaXhxMkE.QX1cDN1wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out 
and submit it!
hacker@variables~storing-command-output:~$ echo $PWN
pwn.college{MvOzHgjuea5aAzWbBVWCaXhxMkE.QX1cDN1wiMwkjNzEzW}
```

## Incorrect tangents I went on
None to report here

## What I learned
We can store outputs of commands into variables via a process called command subsitution. This is syntaxed by '$()' (no backticks here). 

## References
None to note here.