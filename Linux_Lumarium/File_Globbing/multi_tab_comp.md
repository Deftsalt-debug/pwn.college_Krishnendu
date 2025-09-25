# Challenge name
Multiple options for tab completion

## My solve 
**Flag:** `pwn.college{Aas215M4Z6XYsKv7aSyEf_xw1GH.0lN0EzNxwiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege
cat: /challenge/files/pwncollege: No such file or directory
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-
pwncollege-family      pwncollege-flamingo    pwncollege-hacking     
pwncollege-flag        pwncollege-flyswatter  
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-flag
pwn.college{Aas215M4Z6XYsKv7aSyEf_xw1GH.0lN0EzNxwiMwkjNzEzW}
```

## Incorrect tangent I went on
Without realising we were to access a file, I did not implement the usage of cat and thus not allowing me to realistically access the file. Fixed it right after realising this. Also if we see above I accidentally hit backspace before passing the tab completed path, silly error. 

## What I learned
In a fringe case where we have multiple files of similar name scheme, the tab completion does not occur up until the extent where there is a dispute between the filenames/paths. This requires us to hit tab again to see what filenames have a similar scheme and is confusing the completion and move forward with respect to the desired file. Hitting tab again during a dispute seems like a more precise version of ls as we get to only see the listed files similar in naming to the file we want and are in dispute with. 

## References
None to report here. 