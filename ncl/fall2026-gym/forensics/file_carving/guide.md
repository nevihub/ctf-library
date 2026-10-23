# File Carving — walkthrough summary

_Official Trove guide: https://trove.cyberskyline.com/ff55c18374c84109b32b95252309185d (login required)_

## Technique

Identify the file with the file command (it is a PNG), then carve embedded data with binwalk. The extraction reveals a nested tar archive; extract it to find the hidden flag file and count the extractable files.
