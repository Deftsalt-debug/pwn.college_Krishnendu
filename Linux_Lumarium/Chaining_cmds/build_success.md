# Challenge name
Build on success

## My solve
**Flag:** `pwn.college{UuxDONfsJ6EvmYuRiEKIJhUZGbP.0lM0MDOxwiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@chaining~building-on-success:~$ /challenge/first-success && /challenge/second 
Nice chaining! Flag: pwn.college{UuxDONfsJ6EvmYuRiEKIJhUZGbP.0lM0MDOxwiMwkjNzEzW}
```

## Incorrect tangents I went on
None here.

## What I learned
The && operator allows us to add an element of conditionality to our chaining, equivalent to a logic AND, it would only procees with the second successive chain command iff the first one terminates without failure(i.e. it checks for the exit code 0 which is a successful operation). This is helpul in situations where we want to run a command under a contextual premise depending on whether a command succeeds or fails. 

## References
None.