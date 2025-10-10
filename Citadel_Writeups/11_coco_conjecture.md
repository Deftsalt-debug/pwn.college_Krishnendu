# Challenge name
Coco conjecture

## My solve
**Flag:** `citadel{k1ryu_c0c0_h4s_4_g0_4t_4n_uns0lv3d_m4th3m4t1cs_pr0bl3m}` //this is what was on the writeup but I'm pretty sure that the flag was different for us, something about `citadel{1_miss_k1ryu_c0c0}`
This program was a bit excessive but it worked for us.

```py
import socket, sys

def steps(n: int) -> int:
    c = 0
    while n != 1:
        if n % 2 == 0:
            n //= 2
        else:
            n = 3*n + 1
        c += 1
    return c

if len(sys.argv) != 3:
    print("Usage: python3 prog.py <host> <port>")
    sys.exit(1)

HOST, PORT = sys.argv[1], int(sys.argv[2])
ROUNDS = 269

with socket.create_connection((HOST, PORT), timeout=60) as sock:
    fin  = sock.makefile("r", encoding="utf-8", newline="\n")
    fout = sock.makefile("w", encoding="utf-8", newline="\n")

    done = 0
    while done < ROUNDS:
        line = fin.readline()
        if not line:
            print("Server closed connection.")
            break
        text = line.strip()
        print("SERVER:", text)

        if text.startswith("Round"):
            # last word on line is the number
            parts = text.split()
            n = int(parts[-1])
            print("Parsed n =", n)

            ans = steps(n)
            fout.write(str(ans) + "\n")
            fout.flush()
            done += 1
            print(f"[{done}/{ROUNDS}] sent {ans}")
```