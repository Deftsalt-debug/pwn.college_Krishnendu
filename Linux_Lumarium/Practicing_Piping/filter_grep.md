# Challenge name
Filtering Grep using -v

## My solve
**Flag:** `pwn.college{QzNS-NMYhcg7Em90AkQerW6qG0H.0FOxEzNxwiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
pwn.college{QzNS-NMYhcg7Em90AkQerW6qG0H.0FOxEzNxwiMwkjNzEzW}
```

## Incorrect tangents I went on 
None

## What I learned
An alternative argument/option we can pass into grep is -v which inverts the matching of grep and gives us search values of items which do NOT match the argument passed into it, essentially doing the opposite of grep. 

## References 
None to place here.