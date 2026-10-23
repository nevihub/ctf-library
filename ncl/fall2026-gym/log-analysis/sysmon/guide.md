# Sysmon — walkthrough summary

_Official Trove guide: https://trove.cyberskyline.com/3e478798f2f68098832bddf7d27486e5 (login required)_

## Technique

Read the JSON process tree: find the bootstrap executable and its download URL, the main agent executable path, the PowerShell firewall cmdlet, and the verification program. Take the Defender-enabler PID and subtract the firewall-rule timestamp from the Defender-enable timestamp for the elapsed seconds.
