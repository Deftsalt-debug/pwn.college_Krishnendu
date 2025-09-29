# Challenge name
Extracting specific lines of text

## My solve
**Flag:** `pwn.college{4MVKIJN0EIBv3994PbjXiIz49j-.01NxEzNxwiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d' ' | tr -d '\n'
cut: you must specify a list of bytes, characters, or fields
Try 'cut --help' for more information.
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d' ' -f 2 | tr -d '\n'
pwn.college{4MVKIJN0EIBv3994PbjXiIz49j-.01NxEzNxwiMwkjNzEzW}
```

## Incorrect tangents I went on
Here I initially called cut without placing a field specifier thus not giving cut an idea of where to extract the output from, I then assumed the flag characters would preceed the set of numbers and hence set the field specifier to the first column, eventually correcting to it being 2.  

## What I learned
The cut command is a neat manner by which we can seperate specific columns of info which requires two flags and arguments, the -d delimiter speficifng the column delimiter which we as the user can specify as a character where it would terminate the extraction from along with the -f field specifier flag with a numeric argument which tells us exactly under which column of the output we should extract our data from. 

## References 
None.