# Challenge name
Helpful programs

## My solve
**Flag:** `pwn.college{ooiPq5LBS5qJrRFKxKEqn_KY08C.QX3IDO0wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -g GIVE_THE_FLAG
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]
a challenge to make you ask for help: error: argument -g/--give-the-flag: invalid int value: 'GIVE_THE_FLAG'
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 550
hacker@man~helpful-programs:~$ /challenge/challenge -g 550
Correct usage! Your flag: pwn.college{ooiPq5LBS5qJrRFKxKEqn_KY08C.QX3IDO0wiMwkjNzEzW}
```

## Incorrect tangents I went on 
Here I did not catch on to the fact that the GIVE_THE_FLAG argument required an integer and upon a second read of the prompt I realised it was a placeholder for an int value obtained from -p which we have to pass as an argument into -g. 

## What I learned
In cases where there isn't a manpage available, there is a possibility for us to pass a --help argument to prompt us with helpful tips and synopsis' of the arguments available to us for the command. It is sometimes depicted by /? or -h and is another example of a program's documentation which can help us in a pinch and give necessary context to the programs we work with.

## References 
None to note here