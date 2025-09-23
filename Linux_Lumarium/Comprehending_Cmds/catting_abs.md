# Challenge name 
Catting absolute paths

## My solve
**Flag:** `pwn.college{ELz3JJhWQAXDucmnU3s6QjVdwwM.QX5ETO0wiMwkjNzEzW}`

```bash 
Connected!
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{ELz3JJhWQAXDucmnU3s6QjVdwwM.QX5ETO0wiMwkjNzEzW}
```

## Incorrect tangents I went on
None present in this instance

## What I learned
Re-emphasizing on the previous challenge, this is by default allowing us to pass an absolute path as an argument into cat. We're accessing /flag, a file under the root directory, which stores our challenge's flag through cat and as an absolute path. Apparently /flag has generated our flags for each of our previous challenges too. 

## References
None to note