# Challenge name
Comparing files

## My solve
**Flag:** `pwn.college{UgK3eCsbGIJ6y0jpiBmnaTNsUfz.01MwMDOxwiMwkjNzEzW}`

``` bash
Connected!
<iff /challenge/decoys_only.txt /challenge/decoys_and_real.txt                                     <iff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
59a60
> pwn.college{UgK3eCsbGIJ6y0jpiBmnaTNsUfz.01MwMDOxwiMwkjNzEzW}
```

## Incorrect tangents I went on
None here, excuse the formatting my terminal seems to not format this problem for some reason (I've retried this already)

## What I learned
diff here compares the two files for any fallacy in between the two, through the initial line it prompts, we can tell the exact status of where the difference in between the two files emerges. Here in this program, '59a60' gives us the idea that after the 59th line of the original file with only decoys, there emerges an additional line when compared to the 2nd file with real values, the 'a' means that there is an additional line added to the second file (represented by >) and followed by the actual changed line outputted on the command line, giving us our true flag for the challenge. The diff command can further be used to see any changes in lines, here they would be represented by 'c' instead of 'a' and would display file 1's line along with file 2's line so see what exactly is replaced between the two. Thus serving as an excellent means to compare data amongst two files via the terminal instead of eyeballing the two. 

## References
None to state