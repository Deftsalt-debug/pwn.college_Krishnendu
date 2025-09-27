# Challenge name
Exporting variables

## My solve
**Flag:** `pwn.college{EIcjvYZLfKvc-JSUhQR2uKFJ2gx.QXyYTN0wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ export PWN=COLLEGE
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ sh
sh-5.2$ /challenge/run
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great 
job! Here is your flag:
pwn.college{EIcjvYZLfKvc-JSUhQR2uKFJ2gx.QXyYTN0wiMwkjNzEzW}
```

## Incorrect tangents I went on
None to note here.

## What I learned
Variables local to a shell instance are not considered by commands that use them. So if we were to pass them into a seperate command we'd get a blank value as that variable, which is accessed by $. As $ being a prompt of somehting called sh. Invoked as a branch of the main shell and considered as a "child" of the main shell, in this child shell the variable is inaccessable and thus requires and exporting of it. This is done by the command export which takes the variable name as an argument and brings them into an environment variable under the child processes. Thus allowing the child shell to recieve the variable and completing the process.

## References 
None here.