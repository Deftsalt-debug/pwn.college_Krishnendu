# Challenge name
Setting PATH

## My solve 
**Flag:** `pwn.college{4u3zACsqXBvIjMQB5Vq5V-U8CJ3.QX1cjM1wiMwkjNzEzW}`

```bash
hacker@path~setting-path:~$ PATH=/challenge/more_commands/win
hacker@path~setting-path:~$ /challenge/run 
Invoking 'win'....
/challenge/run: line 4: win: command not found
It looks like that did not work... Did you set PATH correctly?
hacker@path~setting-path:~$ PATH=/challenge/more_commands
hacker@path~setting-path:~$ /challenge/run 
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{4u3zACsqXBvIjMQB5Vq5V-U8CJ3.QX1cjM1wiMwkjNzEzW}
```

## Incorrect tangents I went on 
Here I had assumed /challenge/run did not call on win by its bare name and added the win's absolute path into 'PATH' being entirely incorrect as my initial assumption was wrong.

## What I learned
The PATH variable can be modified to adjust and compensate a path to a directory and thus allowing for a launch of a script by its bare name if it is stored under the PATH instead of executing it by its absolute path.

## References
None to note here.