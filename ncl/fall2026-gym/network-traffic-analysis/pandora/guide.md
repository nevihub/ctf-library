# Pandora — walkthrough summary

_Official Trove guide: https://trove.cyberskyline.com/3c506db7881a4e48899380cc08e8c0a9 (login required)_

## Technique

Filter out noise and follow the TCP stream to the custom protocol; decode the length-prefixed requests, note the 2-byte magic ID in decimal and the 32-byte hashes, count the requests, and reassemble the hex responses to reveal the hidden flag.
