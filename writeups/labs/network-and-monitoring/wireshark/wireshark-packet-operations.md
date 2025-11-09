# Wireshark: Packet Operations – TryHackMe

## Overview
- **Platform:** TryHackMe  
- **Focus:** Manipulating packets, searching, and extracting deeper details.  
- **Tools:** Wireshark  

## Key Skills Learned
- Packet marking, coloring rules, and export functions.  
- Using display filters for precision:
  - `http.request.method == "POST"` → show POST requests only.  
  - `dns.qry.name` → filter DNS queries.  
- Exporting objects (HTTP) to recover transferred files.  
- Inspecting TCP flags:
  - `tcp.flags == 2` → pure SYN packets.  
  - `tcp.flags.syn == 1` → matches SYN and SYN-ACK.  

## Lessons Learned
- Beyond filtering, Wireshark can **reconstruct artifacts** like downloaded files.  
- The flags field provides forensic insight into how a connection was initiated or disrupted.  
