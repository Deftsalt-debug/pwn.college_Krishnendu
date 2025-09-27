# Challenge name
Printing exported variables

## My solve
**Flag:** `pwn.college{k_ui-FDlyjkJBTK9gami9KNw1jm.QX4UTN0wiMwkjNzEzW}`

```bash
Connected!                                                                        
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=bd19467c0f89b10a22a0240b770dd6b51e5d3d17c56435e853c51743e25b6017
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{k_ui-FDlyjkJBTK9gami9KNw1jm.QX4UTN0wiMwkjNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env
```

## Incorrect tangents I went on
None to note here

## What I learned 
The env command prints the name and value of every every exported variable under the shell, this is one of the many ways we can access variables under the shell. 

## References
None here.