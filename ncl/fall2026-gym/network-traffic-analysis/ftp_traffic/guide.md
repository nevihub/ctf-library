# FTP Traffic — walkthrough summary

_Official Trove guide: https://trove.cyberskyline.com/da643ef1fbdf44c399de12d273d281b6 (login required)_

## Technique

Follow the FTP TCP streams; filter ftp.response.code == 230 for successful logins; read the server banner for the software and version; inspect the ftp-data stream timing for the deleted file, the uploaded file and its byte count, and the anonymous download.
