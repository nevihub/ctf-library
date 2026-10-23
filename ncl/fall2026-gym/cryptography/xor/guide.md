# XOR — walkthrough summary

_Official Trove guide: https://trove.cyberskyline.com/3b278798f2f68074aa63fc24677380c4 (login required)_

## Technique

Repeating-key XOR. The binary key converts to ASCII 'key'. XOR each ciphertext byte against the repeating key (CyberChef XOR with key 'key', or a short Python loop).
