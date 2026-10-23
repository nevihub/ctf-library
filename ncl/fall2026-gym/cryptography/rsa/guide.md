# RSA — walkthrough summary

_Official Trove guide: https://trove.cyberskyline.com/fafad0e3926b4f808e7616039ca6a6af (login required)_

## Technique

Small-n RSA: factor n by trial division (1079 = 13 x 83), compute phi = (p-1)(q-1), derive d as the modular inverse of e mod phi, then decrypt each c with pow(c, d, n) in Python and convert the numbers to ASCII.
