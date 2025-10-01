# Challenge name
Cracking Passwords

## My solve
**Flag:** `pwn.college{o4moSvYXrjOjgoVfLDrlTpYqvdo.QX3UDN1wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak 
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
0g 0:00:00:20 1% 2/3 0g/s 270.8p/s 270.8c/s 270.8C/s ncc1701d..1022
aardvark         (zardus)
1g 0:00:00:21 100% 2/3 0.04623g/s 269.2p/s 269.2c/s 269.2C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ su zardus
Password: 
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{o4moSvYXrjOjgoVfLDrlTpYqvdo.QX3UDN1wiMwkjNzEzW}
```

## Incorrect tangents I went on
Here I had continuously interrupted the cracking process, aborting the john the ripper process before it output anything assumping I had misinterpreted the challenge. The output the abortion of the process gave was what I assumed was the password to the zardus user, being entirely incorrect.

## What I learned
Here we use the program names john-the-ripper on a leaked /shadow file, a critical aspect of the system which stores all the users passwords encrypted by a one way hash. John here accesses the file and runs multiple algorithms to de-encrypt the passwords stored in /shadow-leak. This challenge simulated a passowrd leak and how we can use it as an advantage to slip into another user's shell by utilising john to get the password to zardus.

## References
None here.