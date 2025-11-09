# Wireshark: Traffic Analysis – TryHackMe

## Overview
- **Platform:** TryHackMe  
- **Focus:** Applying Wireshark to a forensic investigation.  
- **Tools:** Wireshark  

## Key Skills Learned
- DNS analysis to identify suspicious domains (`dns.qry.name`).  
- Tracking attacker IP addresses using SYN scans.  
- Following TCP streams to extract credentials and exfiltrated data.  
- Identifying anomalous HTTP POST requests used for data exfiltration.  

## Lessons Learned
- Real-world IR workflow in Wireshark:
  1. Start with DNS queries (what domains are being contacted).  
  2. Pivot to suspicious sessions (SYN floods, unusual IPs).  
  3. Follow streams to reconstruct the attacker’s actions.  
- Reinforced how **network forensics ties into SOC investigation**.  
