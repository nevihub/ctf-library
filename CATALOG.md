# CTF Library Catalog

Technique and tool index. When facing a new challenge, grep this file
for the technique or tool — it points at the writeup that demonstrates it.

## Cryptography

- Cipher identification → boxentriq cipher identifier, then CyberChef
  (`ncl/fall2025-practice/cryptography.md`, Decoding 1–3: binary, hex, base64, Caesar)
- Caesar cipher → dcode.fr/caesar-cipher (`ncl/fall2025-practice/cryptography.md`, Decoding 2)
- Multitap ABC cipher → dcode.fr/multitap-abc-cipher (`ncl/fall2025-practice/cryptography.md`, Decoding 4)
- RSA small-n factorization → factor n by hand/calculator (n=1079=13×83), derive p, q
  (`ncl/fall2025-practice/cryptography.md`, Decoding 5)
- Decimal-to-ASCII → prepostseo decimal-to-ascii (`ncl/fall2025-practice/cryptography.md`, Decoding 3)

## Password Cracking

- MD5 wordlist → `hashcat -m 0 -a 0 hashes.txt rockyou.txt`
  (`ncl/fall2025-practice/password-cracking.md`, Cracking 1)
- NTLM → ophcrack with small tables (`ncl/fall2025-practice/password-cracking.md`, Cracking 2)
- Mask attack, known prefix → `hashcat -m 0 -a 3 hashes.txt 'SKY-BMYS-?d?d?d?d'`
  (`ncl/fall2025-practice/password-cracking.md`, Cracking 3)
- `$1$` crypt hashes → identify type first, then hashcat mode 500
  (`ncl/fall2025-practice/password-cracking.md`, Cracking 4)
- rockyou.txt → github.com/RykerWilder/rockyou.txt.git mirror

## Log Analysis

- Count/sort/uniq field extraction → awk one-liners on DNS logs
  (`ncl/fall2025-practice/log-analysis.md`, AWS Route 53: resolver IPs, query names,
  city-code → region mapping)
- Pattern: `awk '{print $N}' file | sort | uniq -c | sort -nr | awk 'NR==1{print $2}'`
  for "most common value of field N"
- Android logcat (`system.log`): manufacturer via `grep -ni 'samsung|google|...'`,
  model via `grep -niE '\bSM-[A-Z0-9]+'`, torch on/off via `grep -i 'settorchmode'`,
  battery via `level=` in BatteryService lines, next alarm via `nextAlarm` field
  (epoch 0 = unset) (`ncl/fall2025-practice/log-analysis.md`)

## OSINT

- Domain whois → lookup.icann.org (`ncl/fall2025-practice/osint.md`, WHOIS)
- Vehicle identification → Google Images (`ncl/fall2025-practice/osint.md`, Vehicle)
- Geolocation from photo → gps-coordinates.net (`ncl/fall2025-practice/osint.md`, NASA)
- Blockchain address lookup → explorer for wallet suffix
  (`ncl/fall2025-practice/osint.md`, Colonial Crypto)

## Network Traffic Analysis

- See `ncl/fall2025-practice/network-traffic-analysis.md`

## Forensics

- Corrupted RAR recovery → `unrar l`, `unrar p -inul archive.rar inner.jpg > recovered.jpg`
  (`ncl/fall2025-practice/forensics.md`, Forensics Archive)
- JPEG structure forensics → corrupted byte, compressed data stream, Start of Frame
  (community: "This Bytes" Medium writeup)

## Scanning & Reconnaissance

- (pending Fall 2026 gym ingest)

## Web Application Exploitation

- robots.txt / devtools storage inspection → Burp or browser console
  (`ncl/fall2025-practice/forensics.md` tail notes, Web App)

## Enumeration & Exploitation

- Binary analysis → Ghidra: import, CodeBrowser, decompile entry
  (community: devsurvival "Root Cause" writeup, Spring 2020)

## Meta

- NCL challenge style is often "guess the right tool" — when stuck, the
  catalog's tool column matters more than the technique column.
  (community: pepsipu.com NCL critique)

## NCL Fall 2026 gym additions

- Morse code → dots/dashes = International Morse; CyberChef (`ncl/fall2026-gym/cryptography/beep/`)
- Vigenere with known key → dCode/CyberChef, repeat key (`ncl/fall2026-gym/cryptography/french/`)
- Rail fence transposition → CyberChef Rail Fence Decode, try rail counts; keep punctuation (`ncl/fall2026-gym/cryptography/fencing/`)
- Repeating-key XOR → key from binary, XOR each byte (`ncl/fall2026-gym/cryptography/xor/`)
- Doubly-encoded (binary→base64→text) → decode outside-in (`ncl/fall2026-gym/cryptography/number-bases/`)
- EXIF extraction → metadata2go.com / exif.tools; DMS→decimal for GPS (`ncl/fall2026-gym/osint/meta/`)
- DNS record types → read the RFC (4034 DNSSEC, 3596 IPv6, 1035 delegation) (`ncl/fall2026-gym/osint/lookup/`)
- PGP key lookup → keyserver.ubuntu.com, keys.openpgp.org, pgp.mit.edu; cross-check (`ncl/fall2026-gym/osint/pgp-lookup/`)
- SSL cert inspection → browser padlock > Certificate viewer (`ncl/fall2026-gym/osint/ssl/`)
- Barcode → online-barcode-reader.inliteresearch.com (`ncl/fall2026-gym/osint/barcode/`)
- Web archives → web.archive.org, filter by file type (`ncl/fall2026-gym/osint/owasp/`)
- WHOIS → lookup.icann.org authoritative (`ncl/fall2026-gym/osint/whois/`)

## Scanning & Reconnaissance

- DNS enumeration → dig A/MX/NS/RP/TXT/SRV against given resolver (`ncl/fall2026-gym/scanning-and-reconnaissance/dig/`)
- Port scanning → nmap -Pn (TCP), -sU (UDP), -sV (service detect) (`ncl/fall2026-gym/scanning-and-reconnaissance/nmap/`)
- Git recon → git log, branches, diffs for hidden flags (`ncl/fall2026-gym/scanning-and-reconnaissance/git/`)
- Netcat service interaction → help/version/list/get commands (`ncl/fall2026-gym/scanning-and-reconnaissance/net_track/`)
- Cloud metadata → instance metadata endpoints, AMI lookup (`ncl/fall2026-gym/scanning-and-reconnaissance/metadata/`)
