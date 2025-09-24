# Challenge name 
Linking files

## My solve
**Flag:** `pwn.college{EHkxLVytLZxcTVg3zkg54unHFba.QX5ETN1wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@commands~linking-files:~$ unlink ~/not-the-flag
hacker@commands~linking-files:~$ ln -s /flag ~/not-the-flag
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{EHkxLVytLZxcTVg3zkg54unHFba.QX5ETN1wiMwkjNzEzW}
```

## Incorrect tangents I went on
This is perhaps the longest I took for a challenge, before the above solution I had tried every possible permutation of symlinking possible between the 3 files, /flag, ~/not-the-flag and /challenge/catflag. This all yeilded an error as we cannot establish or override a link between an already present link. This failed attempt to reroute the links all yeilding in error is the central reason as to why it took so long.

## What I learned 
The error on my part forced me to finally search online for references, leading me to discover the unlink command which I used to subsequently remove and relink (using ln) the ~/not-the-flag file into /flag and thus "tricking" the /challenge/catflag to indirectly pull out the /flag file. This was a slightly tricky question but was a fruitful experience, teaching us about symlinks and forcing me out of my comfort zone. The ln command creates a link and the -s flag tells the shell that we're making a soft/symbolic link and we subsequently pass the paths of two files to be linked as arguments, one being the source file we link to and the path/name of the link. This also taught me about hard links which don't seem to be the popular alternative to symlinks due to it's downsides. Links are used in cases where we want two files to point/reflect the same data. We've also learnt the file command which takes a filename(absolute path) as an argument and outputs the type of file it is, along with its link if it is a linking path. 

## References
https://www.freecodecamp.org/news/symlink-tutorial-in-linux-how-to-create-and-remove-a-symbolic-link/