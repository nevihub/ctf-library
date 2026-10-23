# NCL Fall 2025 Practice Games — Password Cracking

_Source: abbey-robinson.com practice games notes (community writeup, Fall 2025 season). Format: challenge name (difficulty) → Notes (tools/methods used) → Challenge (questions with answers inline)._

Password Cracking

Hashing (easy)
Notes
used chat
Challenge
Q1 - 5 points
What is the
MD5 hash of
"LXBWUBEU"

f1e0e04ba5834bf737cc10acb262048b

Q2 - 5 points
What is the
SHA1 hash of
"AJCRVRZE"

1a622a01ea36687c9bef8d46b22bc3d3a0a372a1

Q3 - 5 points
What is the
SHA256 hash
of
"ANBZCNVM"

517a8d1c32eb1b423de55cf9bf07dafedd8d1060c8b5c6ff5021ec9f99f2f86b

Cracking 1 (easy)
Notes
sudo nano cracking1.txt, copy and paste the passwords to be cracked
look up rock you txt github, go to terminal
git clone https://github.com/RykerWilder/rockyou.txt.git
unzip rockyou.txt-main.zip
mv folder to same directory
hashcat -m 0 -a 0 cracking1.txt rockyou.txt-main
Challenge
d9a336ea69220c9383bcf9ab0a86b13d
56gemma56
23438e607b757fd755a00f708cad9f24
loquitakitana
12ec6692013de5cf87f55a4a24f9ee60
monnaka55

Cracking 2 (medium)
Notes
Download ophcrack on windows and the small table
input each hash one by one
Challenge
6AF7253D3F2E0BD51D71060D896B7A46:0FD4E353D19B1507E8421BFA119EA7DE
ofarij22
75F319E42A9540CB1AA818381E4E281B:9D90CD8797F3BF9918B23AC096B8EE6F
lutani83
25CB3174B9E50DBF1AA818381E4E281B:D8E8861BBD7DC37AFFB9EAC45075ACFB
ocuvet73
Cracking 3 (medium)
Notes
make a txt file with your hashes
since we are given more than half of the flag we use hashcat -m 0 -a 3
cracking3.txt 'SKY-BMYS-?d?d?d?d’
tries all combos 0000-9999
Challenge
1650676a6409df93c005c6f040e29bd7
SKY-BMYS-6991
ad12908ab4f2db14915b9a27def5c244
SKY-BMYS-7279
d75c4976711bc318c33d2f5d770728f8
SKY-BMYS-8426
Cracking 4 (hard)
Notes
make a file with all the hashes

Challenge
Q1 - 10 points$1$uxff$sOWmNmM0vFCumj19j0I981
Q2 - 10 points$1$tnck$hhGUKgOmf.fRaG3ZFAMvx1
Q3 - 15 points$1$dgsn$2ZgX3pvquWorGD2Lgjj3W1
Q4 - 35 points$1$vgah$VnxHyh1o3FwMZAvKA5AQo0
Q5 - 50 points$1$lkwc$iOXF5ekiNNyj1KByGFO8s/

PDF (medium)
Zip (hard)
Notes
Challenge
