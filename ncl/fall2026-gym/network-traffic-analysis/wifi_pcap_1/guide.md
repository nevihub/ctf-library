# WiFi PCAP 1 — walkthrough summary

_Official Trove guide: https://trove.cyberskyline.com/288b1672a3824de0b3cd6386057b348b (login required)_

## Technique

Crack the WEP key with aircrack-ng; count and read IVs via the wlan.wep.iv field for the IV count, key size in bits and first IV in hex; decrypt the capture in Wireshark to read the first TCP checksum in hex.
