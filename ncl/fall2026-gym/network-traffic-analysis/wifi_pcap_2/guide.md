# WiFi PCAP 2 — walkthrough summary

_Official Trove guide: https://trove.cyberskyline.com/ca95b65b466c4d3fa3f6b9eb37338b15 (login required)_

## Technique

Same WEP workflow as PCAP 1 with aircrack-ng (128-bit key); read IVs via wlan.wep.iv for the count, key size and first IV; decrypt in Wireshark for the first TCP checksum.
