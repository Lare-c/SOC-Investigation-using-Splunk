# SOC-Investigation-using-Splunk
This repository documents an in-depth SOC investigation conducted on TryHackMe's SOC Challenge using Splunk. The case involves a real-world attack scenario where an adversary compromises a system, establishes a command-and-control (C2) channel, conducts reconnaissance, and exfiltrates sensitive financial data.

**#Attack Breakdown

#Initial Access & C2 Establishment
The attacker downloaded powercat.ps1 from GitHub, a PowerShell-based networking tool used for reverse shells.
They leveraged ngrok, a tunneling service, to create an external connection for remote access.
Reconnaissance & Privilege Enumeration
The attacker ran reconnaissance commands (whoami, systeminfo.exe) to gather system details.
They mapped network shares to identify accessible resources.

Data Discovery & Exfiltration Preparation
Found a shared folder containing financial records.
Used Robocopy.exe to copy the share and compressed the data into exiflt8me.zip.

Data Exfiltration via DNS Tunneling
The attacker used nslookup.exe to perform DNS-based data exfiltration, likely encoding and transmitting the stolen data via DNS queries.
