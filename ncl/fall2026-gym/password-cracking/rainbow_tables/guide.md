# Rainbow Tables — walkthrough summary

_Official Trove guide: https://trove.cyberskyline.com/3f278798f2f6809aa3dad47f2f531509 (login required)_

## Technique

The hashes are LM/NTLM from old Windows servers. Use ophcrack with the free XP rainbow tables; verify the hash type, load the hashes, and read the NT password column for each of the six hash pairs.

> Note: live-target or knowledge-based challenge, no downloadable files.
