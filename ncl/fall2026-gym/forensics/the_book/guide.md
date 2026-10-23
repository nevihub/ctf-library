# The Book — walkthrough summary

_Official Trove guide: https://trove.cyberskyline.com/eaa752e9e94b46a4abea43b7019d0a1b (login required)_

## Technique

Analyze the memory image with Volatility 3: use info, envars and filescan/dumpfiles to identify the OS, computer name and logged-in user, and to locate the file of interest (a SQLite database). Read the database for the real name behind 'cloud', then recover the logged-in user's password via hashdump and crack it.
