# Challenge name
Process Exit Codes

## My solve
**Flag:** `pwn.college{Uh2RhFPOK6iYIrxKlfXJn5pQv7-.QX5YDO1wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@processes~process-exit-codes:~$ /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo $?
199
hacker@processes~process-exit-codes:~$ /challenge/submit-code 199
CORRECT! Here is your flag:
pwn.college{Uh2RhFPOK6iYIrxKlfXJn5pQv7-.QX5YDO1wiMwkjNzEzW}
```

## Incorrect tangents I went on 
None to note here.

## What I learned
This was an insightful look into how processes complete and terminate themselves with respect to exit codes. It is used to differentiate between whether the process succeded in completion or failed in doing so. The exit code of the most recent process in the shell is accessed by the operator '?', we prefix this with the $ to access its actual numeric value (here, in echoing its value). Simple commands that usually succeed terminate with a 0 exit code and a 1 for failure. 

## References
None here.