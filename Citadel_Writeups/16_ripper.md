# Challenge name
The ripper

## My solve
**Flag:** `citadel{fake_flag_4_fake_pl4y3rs}`

Here the challenge name gives us an idea of using John the ripper. Using the command shown below with the files in a terminal directory, we get the flag.
```bash
john --wordlist=./wordlist.txt ./hash.txt
```
Our build of john automatically detected bcrypt so we did not need to specify the hash type.
we show the cracked password using 
```bash
john --show ./hash.txt
```
Thus giving us our flag.