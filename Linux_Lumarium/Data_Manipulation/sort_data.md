# Challenge name
Sorting Data

## My solve 
**Flag:** `pwn.college{A9IDP5UakkiDXpAiCdoK75Gaogt.0FM0MDOxwiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@data~sorting-data:~$ sort -r /challenge/flags.txt
pwn.college{A9IDP5UakkiDXpAiCdoK75Gaogt.0FM0MDOxwiMwkjNzEzW}
and more...
```

## Incorrect tangents I went on 
None to record here.

## What I learned
Sorting a large array of data can be done straight from the shell, using the aptly named 'sort' command. It by default arranges data in alphabetical order, but by passing flag arguments, we can alter this output; -r reverses the ordering (i.e arranges from Z to A); -n does a numeric sort on the data; -u arranges the lines for unique instances of the data alone; -R sorts the data in a random order. 

## References
None.   