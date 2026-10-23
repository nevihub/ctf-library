# SSH — walkthrough summary

_Official Trove guide: https://trove.cyberskyline.com/5213e481daa544fb94001cd51096edbb (login required)_

## Technique

Read the hostname from the log, then list 'Failed password' source IPs in order of first appearance to identify the first, second and third attacker IPs and the targeted username. Find the 'Accepted password' entry for the successful-login IP.
