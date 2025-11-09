# Wireshark: The Basics – TryHackMe

## Overview
- **Platform:** TryHackMe  
- **Focus:** Intro to Wireshark interface, filters, and traffic analysis.  
- **Tools:** Wireshark  

## Key Skills Learned
- Navigating Wireshark UI (packet list, details, and bytes view).  
- Basic filtering:
  - `ip.addr == x.x.x.x` → filter traffic for a specific host.  
  - `tcp.port == 80` → filter traffic on a given port.  
- Identifying TCP 3-way handshakes.  
- Following a TCP stream to reconstruct conversations.  

## Lessons Learned
- Wireshark captures can be overwhelming — filters are critical to narrow the scope.  
- Even unencrypted traffic reveals usernames, file names, and system details quickly.  
