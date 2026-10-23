# Metadata — walkthrough summary

_Official Trove guide: https://trove.cyberskyline.com/cb7a68906cbf4ffdaacbcfbcf54c2164 (login required)_

## Technique

Query the cloud instance metadata endpoints from the live target to collect the availability zone, the IAM credentials role, and the instance type. Look up the AMI ID to determine the OS name and version, then follow the hidden network path to retrieve the flag.

> Note: live-target challenge, no downloadable files.
