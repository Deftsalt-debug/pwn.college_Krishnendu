# Challenge name
Searching for manuals

## My solve 
**Flag:** `pwn.college{wtVoEgLVMi1Q8KzaQ6GkCM66yC1.QX2EDO0wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~$ man --wildcard
What manual page do you want?
For example, try 'man man'.
hacker@man~searching-for-manuals:~$ man man --wildcard
No manual entry for --wildcard
hacker@man~searching-for-manuals:~$ man challenge --wildcard
No manual entry for challenge
No manual entry for --wildcard
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~$ man -k challenge
wtogizakyw (1)       - print the flag!
hacker@man~searching-for-manuals:~$ man wtogizakyw
hacker@man~searching-for-manuals:~$ /challenge/challenge --wtogiz 186
Correct usage! Your flag: pwn.college{wtVoEgLVMi1Q8KzaQ6GkCM66yC1.QX2EDO0wiMwkjNzEzW}
```

## Incorrect tangents I went on
Here I had used wildcard out of sheer curiosity thinking it would help and used incorrect arguments there too, sending the command back into the man manpage and then the nonexistent (randomised) challenge manpage, eventually using the -k argument used to search manpages as the challenge desired.

## What I learned
There exists a manpage for the command man itself, this consists of various arguments we can pass along with man to gauge for various outputs and use-cases. This required a further, more informed use of the search command in a manpage as well as a more detailed read of manpages/documentation. This search for the desired flag/argument to man allowed for us to search for a desired string in the discription or filename of manpages in the system. This giving us the randomised challenge's solution. 

## References
Looked here for a bit out of curiosity and further reading: https://man7.org/linux/man-pages/index.html 