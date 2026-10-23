# Dig — walkthrough summary

_Official Trove guide: https://trove.cyberskyline.com/32778798f2f680bbbefbe257d7955ee4 (login required)_

## Technique

Query DNS records for fortaigan.net using dig against the provided resolver. Run A, MX, NS, RP, TXT and SRV lookups and collect each answer: the domain's IPv4 address, the mail server count and first-priority MX record, the name server's IPv4, the responsible-person record, the TXT record containing the flag, and the SIP service records giving the TCP priority and the SIP host's IPv4 address.

> Note: live-target challenge, no downloadable files.
