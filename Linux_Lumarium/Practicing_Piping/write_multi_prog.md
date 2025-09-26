# Challenge name
Writing to multiple products

## My solve
**Flag:** `pwn.college{olmlG_eNrDSUveNSa0V6oUSORJW.QXwgDN1wiMwkjNzEzW}`

```bash
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the) >(/challenge/planet)
This secret data must directly and simultaneously make it to /challenge/the and 
/challenge/planet. Don't try to copy-paste it; it changes too fast.
799321251121323307
Congratulations, you have duplicated data into the input of two programs! Here 
is your flag:
pwn.college{olmlG_eNrDSUveNSa0V6oUSORJW.QXwgDN1wiMwkjNzEzW}
```

## Incorrect tangents I went on 
I accidentally piped the output of tee /challenge/the into /challenge/planet, yeilding an error. Also forgot to use the process subsitution command, silly errors once more.

## What I learned
Here we pass piping into commands using tee which dupilcates the output as an intput of two more commands using output process subtitution. This is reiterative of the past two challenges and follow the same procedure of knowledge, utilising a mix of piping, named piping (via process subsitution) and the tee command.

## References 
None here.