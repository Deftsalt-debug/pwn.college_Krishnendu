# Challenge name
Translating Characters

## My solve
**Flag:** `pwn.college{4Qzs-LTluXLwAIQ8Nxs4TCkRcuk.01MxEzNxwiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@data~translating-characters:~$ /challenge/run | tr a-zA-Z A-Za-z
yOUR CASE-SWAPPED FLAG:
pwn.college{4Qzs-LTluXLwAIQ8Nxs4TCkRcuk.01MxEzNxwiMwkjNzEzW}
```

## Incorrect tangents I went on
Here I had initially tried to enase the character a-z under quotes and was trying to figure out how exactly it'd fit under syntax (I had also tried to encase the range under curly braces or parantheses), eventually caving in for the simplest method as we've seen above not enclosing anything undeer the string and simply writing the range we want to translate the characters into.

## What I learned
We can pipe in commands into something called tr to modify/translate output from the shell. It takes in two arguments and converts the character provided in the first argument into the ones in the next argument, from the stdout of the command we pipe into it. 

## References
None to note here.
