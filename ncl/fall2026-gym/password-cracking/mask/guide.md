# Mask — walkthrough summary

_Official Trove guide: https://trove.cyberskyline.com/d0a758e85b894a67af88b47cec3316b7 (login required)_

## Technique

The plaintexts follow the fixed pattern SKY-HQNT- followed by four digits, so use a hashcat mask attack: -m 0 -a 3 'SKY-HQNT-?d?d?d?d' against the MD5 hashes.

> Note: live-target or knowledge-based challenge, no downloadable files.
