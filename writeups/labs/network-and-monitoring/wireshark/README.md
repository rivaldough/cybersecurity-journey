# 🧪 Wireshark Labs – TryHackMe

This folder contains my writeups for the Wireshark training rooms on **TryHackMe**.  
Each lab focuses on different aspects of packet analysis, from basics to real-world traffic investigations.  

---

## 📂 Labs

- [Wireshark: The Basics](./wireshark-basics.md)  
  *Introduction to Wireshark interface, filters, and traffic inspection.*  

- [Wireshark: Packet Operations](./wireshark-packet-operations.md)  
  *Working with packets — filtering, coloring, marking, and extracting files from captures.*  

- [Wireshark: Traffic Analysis](./wireshark-traffic-analysis.md)  
  *Investigating real-world attack traffic using DNS queries, TCP flags, and HTTP streams.*  

---

## 🔑 Skills Gained
- Wireshark filtering (`ip.addr`, `tcp.flags`, `http.request`, `dns.qry.name`).  
- Recognizing TCP 3-way handshakes and anomalies in flags.  
- Following TCP streams to reconstruct conversations and extract artifacts.  
- Identifying malicious traffic patterns (scans, exfiltration, C2 comms).  

---

## 📌 Notes
These labs reinforce **blue team and SOC analysis workflows** by practicing:  
1. Filtering large captures into focused datasets.  
2. Pivoting from indicators (domains, IPs) into deeper packet analysis.  
3. Building investigation habits applicable to real-world IR.  
