# Challenge name
Searching Manuals

## My solve
**Flag:** `pwn.college{8Eb0j4wXHq86aa1_2mXH88rkM2C.QX1EDO0wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --val
Initializing...
Correct usage! Your flag: pwn.college{8Eb0j4wXHq86aa1_2mXH88rkM2C.QX1EDO0wiMwkjNzEzW}
```

## Incorrect tangents I went on
Nothing noteworthy

## What I learned
Navigation of a man page is done by the arrow keys. Any specifics we want to search in the page is done by prefixing / to the search term. To search backwards (i.e from the end of the file) we prefix ? instead of /. Navigation amongst the found terms in the man page is done by n to move the to next term and N to move to the previous term. These commands are crucial in the efficient navigation of large manpages where we need to precicely and quickly find a piece of information. 

## References
None. 