# Challenge name 
Exclusionary Globbing

## My solve
**Flag:** `pwn.college{w1atMiLFFtx3-CgbXDhF4qN9bQx.QX2IDO0wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run *[!pwn]*
Your expansion did not expand to the requested files (amazing beautiful 
challenging delightful educational fantastic great happy incredible jovial kind 
laughing magical optimistic queenly radiant splendid thrilling uplifting 
victorious xenial youthful zesty).
Instead, it expanded to:
amazing beautiful challenging delightful educational fantastic great happy incredible jovial kind laughing magical nice optimistic pwning queenly radiant splendid thrilling uplifting victorious wonderful xenial youthful zesty
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{w1atMiLFFtx3-CgbXDhF4qN9bQx.QX2IDO0wiMwkjNzEzW}
```
## Incorrect tangents i went on
Placing a * glob right before the [] exclusionary glob negated the effect of the exclusion of [pwn] thus not giving our deisred output. 

## What I learned
Prefixing a ! or ^ before a set of characters *inside* a [] glob filters out the files having the characters inside [] from the wildcarding process. This furthers hones our ability to look for particular files in our system and allows for a more rounded and precise globbing experience while excluding files of particular formats and characters in our search.

## References
None to record here. 