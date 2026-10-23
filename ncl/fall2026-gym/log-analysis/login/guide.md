# Login — walkthrough summary

_Official Trove guide: https://trove.cyberskyline.com/7c704ee8ab0a4e959360a1486fb60bae (login required)_

## Technique

The log is tab-delimited: use cut on the username, IP and date columns with sort, uniq -c and wc -l to count total attempts, unique usernames, the most common username and its attempt count, the busiest date, and the username seen from the most distinct IPs.
