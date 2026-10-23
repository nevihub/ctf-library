# Kali Linux — walkthrough summary

_Official Trove guide: https://trove.cyberskyline.com/b46fa58080dc4d9b803ca7c7f7c53ecd (login required)_

## Technique

The shadow entry uses yescrypt ($y$). Parse the shadow fields for the username, last-change date, salt and digest. Crack the yescrypt hash with John the Ripper --format=crypt on a yescrypt-capable system using the rockyou wordlist.

> Note: live-target or knowledge-based challenge, no downloadable files.
