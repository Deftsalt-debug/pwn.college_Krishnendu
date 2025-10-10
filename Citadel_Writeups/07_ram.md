# Challenge name
Random Access Memories

## My solve
**Flag:** `citadel{w3_4r3_up_4ll_n1t3_t0_g1t_lucky}`

We have to navigate the commit history of the git repo provided. In which we see 3 files removed and each containing a third of the flag, looking at the history of the commits and past states of the repo we're able to gain a base64 string which we convert into plaintext. Appending the 3 parts gives us the entire flag.