# NCL Fall 2025 Practice Games — Forensics

_Source: abbey-robinson.com practice games notes (community writeup, Fall 2025 season). Format: challenge name (difficulty) → Notes (tools/methods used) → Challenge (questions with answers inline)._

Forensics
Archive (easy)
Notes
To get the first question
file corrupted.rar

unrar l corrupted.rar
To get the flag
unrar l corrupted.rar
unrar p -inul corrupted.rar not_a_flag.jpg > recovered.jpg
open recovered.jpg
Challenge
What is the full name of the file inside the archive? (20 pts)
not_a_flag.jpg
SKY-RARA-7458
Puzzle (medium)
Notes
Challenge
Q1 - 50 points What is the SHA256 checksum (in hexadecimal
representation) of the reassembled file?
Q2 - 50 points What is the flag?

Web App a
use burp
either in inspect console or storage
robots.txt
