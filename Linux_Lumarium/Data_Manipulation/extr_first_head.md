# Challenge name
Extracting first lines with head

## My solve
**Flag:** `pwn.college{wyxEVkSixF3bqVuq3C-ve2KqwuQ.0lNxEzNxwiMwkjNzEzW}`

```bash
hacker@data~extracting-the-first-lines-with-head:~$ /challenge/pwn | head -n 7 | /challenge/college
Congratulations, you piped the right codes!
pwn.college{wyxEVkSixF3bqVuq3C-ve2KqwuQ.0lNxEzNxwiMwkjNzEzW}
```

## Incorrect tangents I went on
Getting too giddy over the question, I misread the directory of /challenge/pwn as /challenge/run(as we generally did in the previous challenges). A silly error on my part.

## What I learned
The head command allows us to see through the output (of another command) line by line, by default it shows 10 lines but using the -n flag with a number passed as an argument, we can specify its limit to display. If something is piped into it, it takes the stdout of the command and splits each string into lines.

## References
None here. 