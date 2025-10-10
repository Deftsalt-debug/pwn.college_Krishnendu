# Challenge name
Feels Like We Only Go Backwards

## My solve
**Flag:** `citadel{f0r_0n3_m0r3_h0ur_1_c4n_r4g3}`

Here we're given a Linux ELF file which is unexecutable without any virtualisation. This led to complications eventually settling on IDA free to decomiple the file. On IDA, we see that the flag is generated at level 3 at sub_1240, where it does this exact calculation on analysis.
for i=0 to 36 we repeat 
`T[i] == key[i] + 5*i + 2*input[i]`
T[i] is the 16-bit values under .rodata xmmword_2330 to xmmword_2360 and rodata:qword_2390 as well as 0x01B1.
key[i] is a sequence of 37 single bytes built inside sub_1240 from constant data in .rodata.

Finally we created a script in py upon extracting the key bytes which does the opposite done in the program

```py
key_bytes = [
 0x03,0x07,0x0b,0x0f,0x0b,0x07,0x03,0x07,0x0b,0x0f,0x0b,0x07,0x03,0x07,0x0b,0x0f,0x0b,0x07,0x03,0x07,0x0b,0x0f,0x0b,0x07,0x03,0x07,0x0b,0x0f,0x0b,0x07,0x03,0x07,0x0b,0x0f,0x0b,0x07,0x03
]

expected = [
 0x00c9,0x00de,0x00fd,0x00e0,0x00e7,0x00ea,0x00f9,0x0120,0x00ff,0x009c,0x0121,0x00fc,0x009f,0x0124,0x0009,0x00ff,0x0164,0x00d9,0x0148,0x012d,0x00cc,0x0141,0x00bc,0x0135,0x0160,0x0175,0x0010,0x015d,0x0154,0x00ef,0x0142,0x015f,0x000f,0x000b,0x0007,0x0003,0x01b1
]

res = []
for i in range(37):
    # solve: T[i] == key[i] + 5*i + 2*input[i]  => input[i] = (T[i] - key[i] - 5*i) // 2
    val = expected[i] - key_bytes[i] - 5 * i
    ch  = (val // 2) & 0xFF
    res.append(ch)

flag = bytes(res)
print(flag.decode('latin1'))
```

Note that `& 0xFF` keeps only the low 8 bits and ensures we interpret the result as a byte (0–255), matching input[i].
res.append(ch) appends the byte value to the result list. 
print(flag.decode('latin1')) prints the bytes as text.