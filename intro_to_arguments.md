# Challenge Name
Introduction to arguments

## My solve
**Flag:** `pwn.college{YSUcNASTPoSKDjaIEV1cPUnRzCw.QX4YjM1wiMwkjNzEzW}`
```bash
hacker@hello~intro-to-arguments:~$ ssh hacker@dojo.pwn.college
/etc/ssh/ssh_config line 52: Unsupported option "gssapiauthentication"
ssh: Could not resolve hostname dojo.pwn.college: Temporary failure in name resolution
hacker@hello~intro-to-arguments:~$ exit
logout

Connected!
hacker@hello~intro-to-arguments:~$ hello hackers
Success! Here is your flag:
pwn.college{YSUcNASTPoSKDjaIEV1cPUnRzCw.QX4YjM1wiMwkjNzEzW}
```
## Incorrect tangents I went on
In this case, I have assumed a connection loss on my client end hence invoking an ssh link without realising that I was still connected to the servers of pwn.college, subsequently realising my error and proceeding with the command call

## What I learned
Here we continue with the command call with the added augment of arguments, this highlights a further parameter we pass onto the command giving an added complexity and personalisaion to making the terminal do what we ask it to. The 'hello' command essentially modulates the echo command on the terminal, printing the string we pass along with the command, i.e the argument and thus completing the challenge

## References 
Whatsapp group tempalate is now going to be further used in future projects