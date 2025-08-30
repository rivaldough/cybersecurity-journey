# 🔒 TryHackMe Lab Write-Up — Zeek

## 🧾 Lab Info
- **Room Name:** Zeek (Bro)
- **Difficulty:** Medium  
- **Category:** Network Security Monitoring  
- **Date Completed:** 2025-08-26

---

## 🎯 Objectives
- Get hands-on with Zeek to analyze network traffic (pcap files).  
- Extract metadata from key logs (conn.log, dns.log, dhcp.log).  
- Write and test custom packet signatures.  
- Explore Zeek scripting for connection patterns, intel logs, file extraction, and more.

---

## 🛠️ Tools & Environment
- **OS Used:** Ubuntu (TryHackMe VM)  
- **Main Tool:** Zeek / Bro  

---

## 🔍 Enumeration / Setup

**Commands and Operations Used**
```bash
# Check versions
zeek -v        # version 4.2.1
zeekctl -v     # ZeekControl module version 2.4.0

# Process sample.pcap and count alerts
zeek -C -r sample.pcap
ls -l       # confirmed 8 alert files generated

# DHCP hostname extraction
cat dhcp.log | zeek-cut host_name

# DNS unique queries
cat dns.log | zeek-cut query | sort -u | wc -l

# Longest connection duration
cat conn.log | zeek-cut duration | sort -nr | head -n1

# Custom HTTP signature search
nano http-password.sig    # rule for "password" in HTTP
zeek -C -r http.pcap -s http-password.sig

# FTP brute attempt detection
nano ftp-bruteforce.sig
zeek -C -r ftp.pcap -s ftp-bruteforce.sig
cat notice.log | zeek-cut uid | sort | uniq -c

# Zeek scripting demonstrations
zeek -C -r smallFlows.pcap
zeek -C -r bigFlows.pcap
zeek -C -r case1.pcap intelligence-demo.zeek
zeek -C -r case1.pcap hash-demo.zeek
zeek -C -r case1.pcap file-extract-demo.zeek
zeek -C -r http.pcap zeek-sniffpass
zeek -C -r case2.pcap geoip-conn
zeek -C -r case2.pcap sumstats-counttable.zeek
```

---

**## 📚 Key Takeaways ##**

- Zeek excels at creating structured logs (e.g. conn.log, dns.log) from packet captures.
- Custom signatures in .sig files let you flag specific traffic patterns (like HTTP passwords or FTP brute force attempts).
- Zeek scripting enables deeper analysis: connection counting, file extraction, geolocation, intel logging.
- Useful for enriching SOC visibility beyond signature-based monitoring (e.g., Snort), with comprehensive flow and metadata logs.
