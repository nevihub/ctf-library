# Packet Dissection — walkthrough summary

_Official Trove guide: https://trove.cyberskyline.com/b0f020a3d5724b0bb71917316c132ce0 (login required)_

## Technique

Parse the IPv4 header at the standard byte offsets: read the header checksum in hex, the TTL, and the source and destination IP addresses (converting hex with CyberChef as needed).

> Note: browser-based lab, no downloadable files.
