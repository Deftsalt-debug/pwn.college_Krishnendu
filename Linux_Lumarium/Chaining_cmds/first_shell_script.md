# Challenge name
Your first shell script

## My solve
**Flag:** `pwn.college{UoeQkdss-hUkEwEoXbp1jObBJ5e.QXxcDO0wiMwkjNzEzW}`

```bash 
hacker@chaining~your-first-shell-script:~$ nano x.sh
hacker@chaining~your-first-shell-script:~$ bash x.sh
Great job, you've written your first shell script! Here is the flag:
pwn.college{UoeQkdss-hUkEwEoXbp1jObBJ5e.QXxcDO0wiMwkjNzEzW}
```

## Incorrect tangents I went on
This was confusing because as we are using ssh solely, we can't really call on any text editor(at least on mac) thus making me move into choosing nano for my command line editor. This came to me after multiple tries of failed attempts trying to pipe into x.sh somehow and just mashing 'bash x.sh' repeatedly expecting something to appear. 

## What I learned
Another way of chaining is done by placing the multiple commands to be executed into a shell script (.sh) and executing the script by passing it as an argument to an instance of our bash shell. This invokation of bash through the file allows for the terminal to read off of the shell script in the place of the user input. Creation of shell scripts is done via ssh using a terminal text editor, here I've used nano to create and edit the shell script which gives us an interactive, gui/IDE-like environment to write our code/commands all localised under the shell. 

## References
https://www.geeksforgeeks.org/linux-unix/how-to-create-a-shell-script-in-linux/ 