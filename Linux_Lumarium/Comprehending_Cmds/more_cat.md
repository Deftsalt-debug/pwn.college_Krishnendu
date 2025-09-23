# Challenge name
More catting practice

## My solve
**Flag:** `pwn.college{0Jt7abO6PnTyL4w5-PS5xMn2zrU.QXwITO0wiMwkjNzEzW}`

```bash
Connected!
You cannot use the 'cd' command in this level, and must retrieve the flag by
absolute path. Plus, I hid the flag in a different directory! You can find it
in the file /usr/include/sepol/flag. Go cat it out **without** cding into that
directory!
hacker@commands~more-catting-practice:~$ cat /usr/include/sepol/flag
pwn.college{0Jt7abO6PnTyL4w5-PS5xMn2zrU.QXwITO0wiMwkjNzEzW}
```

## Incorrect tangents I went on
None to say this time

## What I learned
This is reiterative of the previous two challenges, this time we aren't allowed to cd into any directory and list (ls) anything to find the flag file. The termnial's predetermined message though, kindly offers us the file's absolute path, which we can thankfully pass as an argument into cat. Thus catting the flag file for us. The purpose of this challenge was to essentially get us comfortable with catting and how it can take a somewhat complex and long looking path and still extract the desired file as long as we have its absolute path.  

## References
None to add