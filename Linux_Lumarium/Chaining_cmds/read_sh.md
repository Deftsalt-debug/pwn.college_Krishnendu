# Challenge name 
Reading shell scripts

## My solve
**Flag:** `pwn.college{QFzsknjQkUMOuYk0uafnnxDXS0D.0lMwgDOxwiMwkjNzEzW}`

```bash 
Connected!                                                                        
hacker@chaining~reading-shell-scripts:~$ cat /challenge/run
#!/opt/pwn.college/bash

read GUESS
if [ "$GUESS" == "hack the PLANET" ]
then
	echo "CORRECT! Your flag:"
	cat /flag
else
	echo "Read the /challenge/run file to figure out the correct password!"
fi
hacker@chaining~reading-shell-scripts:~$ /challenge/run
hack the PLANET
CORRECT! Your flag:
pwn.college{QFzsknjQkUMOuYk0uafnnxDXS0D.0lMwgDOxwiMwkjNzEzW}
```

## Incorrect tangents I went on
None to report here.

## What I learned
We can read shell scripts in a multitude of ways, I've used nano and vim in these instances (although they are editors) but here I've used cat since we only need to read the file and not write to it. It's insinctive to understand shell scripts as they seem to be useful in application of basic system level tasks.

## References
None to note here.