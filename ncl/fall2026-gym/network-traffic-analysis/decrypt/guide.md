# Decrypt — walkthrough summary

_Official Trove guide: https://trove.cyberskyline.com/897053bf2dfc44ccae0ca796d2493e8a (login required)_

## Technique

Load the TLS key log into Wireshark to decrypt the session; read the cipher suite from the Server Hello, the certificate's domain, and confirm the flag in the decrypted HTTPS stream.
