# Hack the Gibson — walkthrough summary

_Official Trove guide: https://trove.cyberskyline.com/39578798f2f680d9a3e1ca70d95e41ff (login required)_

## Technique

The XMI wraps base64-encoded IBM NETDATA: decode and extract it to reach the archive inside, unzip it, and convert EBCDIC to ASCII. The password hashes are RACF (z/OS), so crack the FIREID and V0421 hashes with John the Ripper --format=RACF.
