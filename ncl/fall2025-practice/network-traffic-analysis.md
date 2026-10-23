# NCL Fall 2025 Practice Games — Network Traffic Analysis

_Source: abbey-robinson.com practice games notes (community writeup, Fall 2025 season). Format: challenge name (difficulty) → Notes (tools/methods used) → Challenge (questions with answers inline)._

Network Traffic Analysis
Retriever (easy)
Notes
1. 1st packet → internet protocol → src
2. 1st packet → internet protocol → dst

3.

4. follow TCP steam
5. follow TCP steam
6. follow TCP steam
7. follow TCP steam
Challenge
Q1 - 10 points What is the client's IP address?

22.183.56.37

Q2 - 10 points What is the server's IP address?

22.183.57.188

Q3 - 10 points What TCP port are they communicating over?

143

Q4 - 10 points What is the name of the server software?

Dovecot

Q5 - 15 points What is Tom's password?

mashandgravy

Q6 - 15 points What is the email address of the malicious actor? b33b0p@wonkey.leaks
Q7- 20 points Where does the actor want to meet Tom?

Paris

Cracking (medium)
Notes
1.
Challenge
Q1 - 10 points What channel was the victim network operating on?

Channel 4

Q2 - 10 points What is the ESSID of the wifi network that was hacked?
Q3 - 10 points What is the MAC address of the device generating traffic
that makes cracking the password on the wifi network possible?
Q4 - 10 points What company is assigned the OUI of the access point?
Q5 - 30 points What is the wireless password (in hex)?

TV (medium)
u can use pcap analyzer → a packets.com
Secret (hard)

Retriever — Wireshark notes (from source PDF screenshots):
IPv4 Src: 22.183.56.37 → Dst: 22.183.57.188; TCP Dst Port: 143 (IMAP).
Workflow: check 1st packet internet protocol src/dst, then follow TCP stream.
