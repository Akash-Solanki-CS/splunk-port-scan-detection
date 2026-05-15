# Splunk Port Scan Detection Lab

## Overview
This project demonstrates reconnaissance and port scan detection using Splunk SIEM and UFW firewall logs.

## Tools Used
- Kali Linux
- Nmap
- Ubuntu
- UFW Firewall
- Splunk Enterprise
## Detection Queries
- Top SRC IPs
- Blocked ports
- SYN scan detection
- Recon detection using multiple destination ports

## Skills
- SIEM basics
- Log analysis
- False positive reduction

## Attack Simulation
Performed SYN scan using:

```bash
nmap -sS 192.168.56.103
```

## Log Collection

```bash
/var/log/ufw.log
```

## SPL Queries
```
source="ufw.log" | top SRC

source="ufw.log" "UFW BLOCK"

source="ufw.log" SYN 
