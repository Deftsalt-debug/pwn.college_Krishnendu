# Challenge name
Executable Shell Scripts

## My solve
**Flag:** `pwn.college{IrYky-kBiy1wtNAX4sqRGam-eTQ.QX0cjM1wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@chaining~executable-shell-scripts:~$ nano x.sh
hacker@chaining~executable-shell-scripts:~$ chmod a+x ./x.sh
hacker@chaining~executable-shell-scripts:~$ ./x.sh
Congratulations on your shell script execution! Your flag:
pwn.college{IrYky-kBiy1wtNAX4sqRGam-eTQ.QX0cjM1wiMwkjNzEzW}
```

## Incorrect tangents I went on
Here I accidently misread the prompt given to us and did not make the .sh file executable, thus leading the script execution to not take place.

## What I learned
We can essentially run shell scripts as an executable without using the bash command and subsequently passing it as an instance of the shell. This is done by modifying the script's perms by using chmod to allow its execution parameter and calling its path. Thus not even requiring bash to be called here

## References
None here.