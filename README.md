# Task-1
Task 1: Scan Your Local Network for Open Ports

Tools Used
- Nmap
- Command Prompt (Windows)

Command Used
nmap -sS 192.168.1.0/24

Open Ports Found after running TCP SYN scan on Nmap

PORT     STATE SERVICE
80/tcp   open  http
135/tcp  open  msrpc
139/tcp  open  netbios-ssn
445/tcp  open  microsoft-ds
902/tcp  open  iss-realsecure
912/tcp  open  apex-mesh
8090/tcp open  opsmessaging

Risks Identified
Ports 139 & 445 (NetBIOS & SMB): Common targets for lateral movement and ransomware.

Port 135 (MSRPC): Can be used in DCOM attacks if misconfigured.

Port 8090 (Ops Messaging): May expose admin panels or backends.

Port 80 (HTTP): If there's no HTTPS, traffic is unencrypted — vulnerable to sniffing or MITM.

Ports 902/912: Used by VMware or other enterprise tools — make sure they're up-to-date and access-restricted.
