# NMAP — walkthrough summary

_Official Trove guide: https://trove.cyberskyline.com/a92ccb5089604e069f30e7436394efb3 (login required)_

## Technique

Scan the live target with nmap. Use nmap -Pn for a TCP scan to find the three lowest open TCP ports, nmap -sU for a UDP scan to find the lowest open UDP port, and nmap -sV service detection to identify the software name and version listening on TCP port 16080.

> Note: live-target challenge, no downloadable files.
