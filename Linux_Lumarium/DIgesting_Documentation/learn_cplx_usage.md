# Challenge name
Learn Complex Usage

## My solve
**Flag:** `pwn.college{Eb7RkRRHR9WhTpBw0JY4zNxNDzW.QX1ITO0wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /challenge/DESCRIPTION.md
Correct argument! Here is the /challenge/DESCRIPTION.md file:
While using most commands is straightforward, the usage of some commands can get quite complex.
For example, the arguments to commands like `sed` and `awk`, which we're definitely not getting into right now, are entire programs in an esoteric programming language!
Somewhere on the spectrum between `cd` and `awk` are commands that take arguments to their arguments...

This sounds crazy, but you've already encountered this with the `find` level in [Basic Commands](/linux-luminarium/commands).
`find` has a `-name` argument, and the `-name` argument itself takes an argument specifying the name to search for.
Many other commands are analogous.

Here is this level's documentation for `/challenge/challenge`:

> Welcome to the documentation for `/challenge/challenge`! This program allows you to print arbitrary files to the terminal, when given the `--printfile` argument. The argument to the `--printfile` argument is the path of the flag to read. For example, `/challenge/challenge --printfile /challenge/DESCRIPTION.md` will print out the description of the level!

Given that documentation, go get the flag!
hacker@man~learning-complex-usage:~$ ls
Desktop  a  flag  not-the-flag
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{Eb7RkRRHR9WhTpBw0JY4zNxNDzW.QX1ITO0wiMwkjNzEzW}
```

## Incorrect tangents I went on
None in this instance

## What I learned
This is iterative off of the previous challenge, that being of using documentation and passing arguments from so as prescribed. This does add an extra layer of complexity by us passing two arguments to /challenge/challenge and the documentation not nesessarily giving us the exact steps to proceed with. But it does tap into previously learnt concepts, that being of cd and ls.

## Referneces
None to note here. 