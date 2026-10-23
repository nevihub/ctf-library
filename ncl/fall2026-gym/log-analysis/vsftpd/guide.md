# VSFTPD — walkthrough summary

_Official Trove guide: https://trove.cyberskyline.com/a9aad5ab10334ac4ab37bdd04058e1ba (login required)_

## Technique

Grep for login, mkdir, upload and download lines; use awk on the byte-count fields and sum per user. Find ftpuser's first IP, the first and last created directories, the most used file extension, the other username and its IP, bytes uploaded by each user, bytes downloaded by ftpuser, and the suspicious login IP.
