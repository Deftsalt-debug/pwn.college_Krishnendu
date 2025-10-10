# Challenge name
Echoes and Pings

## My solve
**Flag:** `citadel{1_r34lly_w4nt_t0_st4y_4t_y0ur_h0us3}`

Here upon analysis of the IMCP section in the .pcap file via wirreshark we see the file header of a .jpg file. Across the two we see a file header and footer. Thus this tells us that the flag must be in the image passed via IMCP. This script was vibecoded partially, also used scapy to extract the flag. 

```py
from scapy.all import rdpcap, ICMP, Raw

packets = rdpcap("challenge.pcap")
pieces = []
for pkt in packets:
    if pkt.haslayer(ICMP) and pkt.haslayer(Raw):
        pieces.append((pkt[ICMP].seq if hasattr(pkt[ICMP], "seq") else 0, pkt[Raw].load))

pieces.sort(key=lambda item: item[0])

with open("flag.jpg", "wb") as outf:
    outf.write(b"".join(data for _, data in pieces))
```