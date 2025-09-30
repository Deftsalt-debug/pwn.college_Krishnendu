# Challenge name 
Other users with su

## My solve
**Flag:** `pwn.college{4kikQJ1lJnw3vniF72XlDYhsAJ2.QX2UDN1wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@users~other-users-with-su:~$ su zardus
Password: 
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{4kikQJ1lJnw3vniF72XlDYhsAJ2.QX2UDN1wiMwkjNzEzW}
```

## Incorrect tangents I went on 
None to report here.

## What I learned 
The su command, when passed without any arguments, directly accesses the root user, but upon passing a specific user's name as an argument. Su begins to allow us to access that specific user's shell. This adds a layer of specifics to su and allows us to pin su to a specifc user we want to access.

## References
None here to append. 