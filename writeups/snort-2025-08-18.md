# 🔒 TryHackMe — Snort

## 🧾 Lab Info
- **Room Name:** Snort
- **Difficulty:** Medium
- **Category:** Network Security and Traffic Analysis
- **Date Completed:** 2025-08-18

---

## 🎯 Objectives
- Learn Snort operating modes (sniffer, packet logger, IDS).
- Write and test custom detection rules.
- Analyze alerts from captured traffic (pcaps).
- Understand how IDS fits into real-world network defense.

---

## 🛠️ Tools & Environment
- **OS Used:** Ubuntu
- **Main Tools:** Snort
- **Config Paths:** `/etc/snort/snort.conf`, `/etc/snort/rules/local.rules`, `/Desktop/Task-Exercises/Exercise-Files/TASK-9/local-rules`  
---

## 🔍 Enumeration / Setup

**Commands and Rules Used**
```bash
# Commands
sudo snort -r logname.log -X
sudo snort -dev -K ASCII -l .
sudo snort -r logname -n 10
sudo snort -r logname 'tcp and port 80'
sudo snort -c /etc/snort/snort.conf -A full -l .
sudo snort -c /etc/snort/snort.conf -A full -l . -r mx-1.pcap
sudo snort -c /etc/snort/snort.conf -A full -l . --pcap-list="mx-2.pcap mx-3.pcap"

# Custom Rules
alert icmp any any <> any any (msg:"ID FOUND"; id:35369; sid:100001; rev:1;)
alert tcp any any <> any any (msg:"FLAG FOUND"; flags:S; sid:100002; rev:1;)
alert tcp any any <> any any (msg:"FLAG FOUND"; flags:PA; sid:100003; rev:1;)
alert udp any any <> any any (msg:"SAME-IP FOUND"; sameip; sid:100004; rev:1;)
```

---

## 📚 Key Takeaways
- Learned the three main Snort modes: **sniffer, packet logger, IDS**.  
- Practiced writing **custom Snort rules** (ICMP, TCP, UDP).  
- Gained experience analyzing **pcap traffic** with different output formats.  
- Reinforced the importance of **rule IDs (SIDs/REV)** for rule management.  
- Saw how IDS can be tuned for **specific attacks or anomalies**.  
- Learned to structure and document labs for a professional GitHub portfolio.

## 🔄 Additional Practice
Completed the “Snort Challenge – The Basics” on TryHackMe as reinforcement.
