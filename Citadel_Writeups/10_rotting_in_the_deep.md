# Challenge name
Rotting in the deep

## My solve
**Flag:** `citadel{br0_r34lly_unr0tt3d_m3_b4ck_t0_l1f3}`

Here the python script given to us tells us exactly what we must do, essentially reversing the shift by subtracting 3 from each integer in the flag. Adding it to flag and then use the function long_to_bytes on the flag. 

```py
from Crypto.Util.number import long_to_bytes as _ltb

cipher_text = (
    "6895840967002953721051398351211751734500850509315790892845302801984496338433"
    "523326225010635779036738800318"
)

pieces = []
for ch in cipher_text:
    # convert char to its numeric value, subtract 3 mod 10, collect as string
    pieces.append(str((ord(ch) - 48 - 3) % 10))

numeric = int("".join(pieces))
plaintext = _ltb(numeric)
print(plaintext)
```