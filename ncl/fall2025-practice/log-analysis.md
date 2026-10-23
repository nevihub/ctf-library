# NCL Fall 2025 Practice Games — Log Analysis

_Source: abbey-robinson.com practice games notes (community writeup, Fall 2025 season). Format: challenge name (difficulty) → Notes (tools/methods used) → Challenge (questions with answers inline)._

Log Analysis
AWS Route 53 (easy)
Notes
1- scrolled to the bottom to see last number
2 - FILE=route53.log , awk '{print $(NF-1)}' route53.log | sort | uniq -c | sort -nr |
awk 'NR==1{print $2}'

3- awk '$4!="-"{print tolower($4)}' route53.log | sort | uniq -c | sort -n | awk
'NR==1{print $2}'

4- awk '$NF != "-" && $NF ~ /\/[0-9]+$/ {print $NF}' route53.log \
| sort | uniq -c | sort -nr | awk 'NR==1{print $2}'
5- awk '{print substr($2,1,16)}' route53.log | sort | uniq -c | sort -nr | awk
'NR==1{print $2}'

6- awk '{print $(NF-2)}' route53.log | sort | uniq -c | sort -nr | awk 'NR==10{print $2}'
7- awk '{ # find the token that looks like an AWS resolver location, e.g. IAD89C3, DFW55-C1 for(i=1;i<=NF;i++){ if ($i ~ /^[A-Z]{3}[0-9]+-C[0-9]+$/) {
city = substr($i,1,3) # keep only the first 3 letters => city code
count[city]++
break } } } END{ for (c in count) print count[c], c }' route53.log | sort -nr |
awk 'NR==10{print $2}’
8- grep -i 'cityinthe.cloud' route53.log \| awk '{print $(NF-2)}' \| sed -E 's/^([AZ]{3}).*/\1/' \| sort | uniq -c | sort -nr | awk 'NR==1{print $2}' \| awk
'BEGIN{r["IAD"]="us-east-1"; r["JFK"]="us-east-1"; r["EWR"]="us-east-1";
r["BOS"]="us-east-1";r["ATL"]="us-east-1"; r["MIA"]="us-east-1";
r["DFW"]="us-east-1";r["CMH"]="us-east-2"; r["ORD"]="us-east-

2";r["SFO"]="us-west-1"; r["LAX"]="us-west-1";r["SEA"]="us-west-2";
r["PDX"]="us-west-2"; r["PHX"]="us-west-2"; r["DEN"]="us-west-2"} {print
(r[$0]?r[$0]:"unknown("$0")")}’
Challenge
Q1 - 5 points How many total requests are recorded in this log?

4519

Q2 - 15 points What is the IP address of the resolver that made the
largest number of requests?

155.225.66.25

Q3 - 15 points What is the least requested domain name?

backup.cityinthe.cloud

Q4 - 15 points What is the client subnet (in CIDR notation) that made
192.154.46.0/24
the largest number of requests?
Q5 - 15 points Which minute of the day had the largest number of
requests?

19:35

Q6 - 25 points Which city received the 10th largest number of
requests?

Miami

Q7 - 10 points What AWS region does cityinthe.cloud use for its
Virtual Private Cloud?

us-east-1

Devices (medium)
Notes
1- awk '!/^\/\// { gsub(/\[|\]/,"",$2); print $2 }' devices.log | sort -u | wc -l
2- awk '!/^\/\// { gsub(/[{}]/,"",$3); print $3 }' devices.log | sort -u | wc -l
3- awk '!/^\/\// { gsub(/%/,"",$4); sum+=$4; n++ } END { printf("%.0f\n", sum/n)
}' devices.log
4- awk '!/^\/\// && $3=="{POWER_METER}" { total+=$5 } END { print total }'
devices.log
5- awk '!/^\/\// && $3=="{POWER_METER}" { day=substr($1,1,10);
usage[day]+=$5 }
END { for (d in usage) print d, usage[d] }' devices.log \
| sort -k2,2nr | head -1
6- awk '!/^\/\// && $3=="{POWER_METER}" { day=substr($1,1,10);
usage[day]+=$5 }
END { for (d in usage) print d, usage[d] }' devices.log \
| sort -k2,2nr | head -1 | awk '{print $2}'
Challenges
Q1 - 10 points How many different devices are present in the log?

Q2 - 10 points How many different device types are present in the log?

Q3 - 20 points What is the average battery life of all the devices throughout

the duration of the log? (Round to the nearest whole percent)
Q4 - 15 points What is the total power usages reported from the power
meters?

142970

Q5 - 25 points On what day was the most power used?

2022-03-24

Q6 - 30 points How much power was consumed that day?

26380

mobile (hard)
Notes
1- awk 'NF>4 && $5=="D"' system.log | wc -l
2- grep -iE 'build fingerprint|ro\.build\.version|Android [0-9]|OS version'
system.log | head -20 → look at the first line
3- grep -i 'onAuthenticationSucceeded' system.log | wc -l
4- grep -c -F 'FingerprintService: handleAuthenticated: false' system.log
5- grep -i 'Authentication' system.log

6- grep -i 'ssid' system.log
7- grep -i 'level' system.log

Notes P2
8- grep -niE 'AlarmClock|nextAlarm|DeskClock|com\.android\.deskclock'
system.log

9- grep -i 'flashlight' system.log
- grep -i 'settorchmode' system.log

ON = 13:08:24.623 → ((13×3600 + 8×60 + 24)×1000 + 623) = 47,304,623 ms
OFF = 13:09:29.919 → ((13×3600 + 9×60 + 29)×1000 + 919) = 47,369,919 ms
OFF − ON = 47,369,919 − 47,304,623 = 65,296 ms
10- grep -niE
'samsung|google|motorola|oneplus|xiaomi|huawei|oppo|vivo|sony' system.log |
head

11-grep -niE '\bSM-[A-Z0-9]+' system.log

Challenge
Q1 - 5 points How many debug messages are present in the log?

10699

Q2 - 5 points What OS is this device running?

android

Q3 - 10 points How many times was finger print authentication
accepted?

Q4 - 10 points How many times was finger print authentication
denied?

Q5 - 15 points What is the application ID (other than the lock-screen)
that successfully used finger print authentication?

com.x8bit.bitwarden

Q6 - 15 points What is the name of the WiFi network the phone is
connected to?

BBNET5

Q7 - 20 points What is the battery percentage at the end of the log?
NOTE: This question only allows maximum of 5 attempts, you have 5
attempts remaining.

Q8 - 20 points What date and time is the alarm set for? (in UTC)

2021-03-11 15:00

Q9 - 20 points How long (in milliseconds) was the flashlight on?

65,296

Q10 - 5 points What company is the manufacturer of the phone?

samsung

Q11 - 25 points What is the full model number of the phone?

SM-G991U1

## Android system.log (logcat) analysis

Challenge: given an Android `system.log`, answer questions with grep.
Technique notes (from screenshots in the source PDF):

- Phone manufacturer: `grep -ni 'samsung|google|motorola|oneplus|xiaomi|huawei|oppo|vivo|sony' system.log | head` → Samsung
- Phone model: `grep -niE '\bSM-[A-Z0-9]+' system.log` → SM-G991U1
- Flashlight on/off times: `grep -i 'settorchmode' system.log` → CameraManager setTorchMode cameraId=0 enabled=true at 13:08:24, enabled=false at 13:09:29
- Battery level: BatteryService lines, `level=` field → 92
- Fingerprint auth failures: FingerprintService `onAuthenticationFailed()` lines
- Next alarm: AlarmProvider / ScheduleCalendar `nextAlarm` field → Wed Dec 31 16:00:00 PST 1969 (epoch 0 = no alarm set)
