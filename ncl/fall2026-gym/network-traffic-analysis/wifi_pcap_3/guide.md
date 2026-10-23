# WiFi PCAP 3 — walkthrough summary

_Official Trove guide: https://trove.cyberskyline.com/5c795a418e19432ca84093f469c0d25e (login required)_

## Technique

Read the router MAC and ESSID from beacons; crack the WPA key with aircrack-ng and rockyou; decrypt to follow the HTTP admin session for the router IP, manufacturer, model, firmware, release and admin-login IP; filter deauthentication frames for the two victim MACs.
