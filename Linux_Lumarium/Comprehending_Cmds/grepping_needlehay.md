# Challenge name
Grepping for a needle in a haystack

## My solve 
**Flag:** `pwn.college{YlBjxpBdyXNtGRu_umHN4jUa8ML.QX3EDO0wiMwkjNzEzW}`

```bash
Connected!
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{YlBjxpBdyXNtGRu_umHN4jUa8ML.QX3EDO0wiMwkjNzEzW}
```

## Incorrect tangents I went on
It was very tempting to see if we could somehow cat the file, safe to say I'm not doing what the prompt in pwn.college tells me not to do. 

## What I learned
The 'grep' command/prompt is a powerful tool as a subsitute for cat, in this instance where catting a file prompts an impossible task to find the flag (or any piece of data to be frank) as well as in instances where we deal with large files, we use grep which takes in an input string (to search for) and the absolute file path giving us the exact string we searched for in the file by printing it into the terminal. Here we search for the flag by passing "pwn.college" as the argument string to be searched as well as the path for data.txt where grep will grab the flag string from and print it subsequently. I assume there are further situations where we can use grep in different ways as we progress through this module. 

## References
None to put here.
 