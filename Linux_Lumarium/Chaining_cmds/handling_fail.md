# Challenge name
Handling Failure

## My solve
**Flag:** `pwn.college{EZWbiULvisr6PrsgtOOJy7TdNSx.01M0MDOxwiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@chaining~handling-failure:~$ /challenge/first-failure || /challenge/second 
Nice chaining! Flag: pwn.college{EZWbiULvisr6PrsgtOOJy7TdNSx.01M0MDOxwiMwkjNzEzW}
```

## Incorrect tangents I went on
None to note here

## What I learned
The OR operator (||) is another way of conditionally chaining commands and it operates exactly opposite to the AND operator. Here it only chains the commands if the first one results in a failure (exit code 1), therefore it either sucessfully executes the first command or executes the second one(thus chaining if the first fails). It is used during error handling and cases where a failure fallback is required.

## References 
None here.