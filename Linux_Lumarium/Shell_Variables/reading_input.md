# Challenge name
Reading Input

## My solve
**Flag:** `pwn.college{o3ddg59Kjv1GGuXidKmxPCIbfVe.QX4cTN0wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@variables~reading-input:~$ read -p "INPUT: " PWN
INPUT: COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{o3ddg59Kjv1GGuXidKmxPCIbfVe.QX4cTN0wiMwkjNzEzW}
```

## Incorrect tangents I went on
None to report on this front.

## What I learned
The read command allows for the shell to resemble a more interactive element akin to modern interafaces. This allows for us as the user to set a value to the variable as an input. This is done by passing the variable as an argument to the command. We can also send over a string of text as a prompt to the user through the argument/option of -p which can take a string bounded in double quotes to send to the user before they enter their output. Note that read takes in our stdin.

## References
None to record here.