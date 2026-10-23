# Custom File Format — walkthrough summary

_Official Trove guide: https://trove.cyberskyline.com/545a23ed71d047b19cfdcb49bfd69376 (login required)_

## Technique

Parse the big-endian binary format per the challenge spec (CyberChef or a script) to extract the header fields: hostname, plaintext flag and creation date in UTC, plus the entry records. Aggregate with awk for entry count, total bytes, unique IPs, the top sender IP and its bytes, and the busiest day.
