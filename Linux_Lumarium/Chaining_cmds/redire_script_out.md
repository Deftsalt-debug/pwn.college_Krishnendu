# Challenge name
Redirecting Script Output

## My solve
**Flag:** `pwn.college{kNjvSGBfFhxUGmmH47UQYa2441U.QX4ETO0wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@chaining~redirecting-script-output:~$ nano x.sh
hacker@chaining~redirecting-script-output:~$ bash x.sh | /challenge/solve 
Correct! Here is your flag:
pwn.college{kNjvSGBfFhxUGmmH47UQYa2441U.QX4ETO0wiMwkjNzEzW}
```

## Incorrect tangents I went on 
None to note here

## What I learned
Here we are answered the question of whether we can pipe a shell script into a command which is absolutely possible. The shell treats a .sh script as another set of commands and thus allows for its redirection and piping. 

## References
None to note here.