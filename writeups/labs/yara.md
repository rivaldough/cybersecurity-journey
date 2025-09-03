# 🔒 TryHackMe — YARA

## 🧾 Lab Info
- **Room Name:** YARA
- **Difficulty:** Easy
- **Category:** Cyber Threat Intelligence
- **Date Completed:** 2025-08-08

---

## 🎯 Objectives
- Understand YARA rule structure (meta, strings, condition).
- Write rules to detect simple indicators and PE traits.
- Scan files and folders, test true/false positives.
- Use tags, imports, and common condition helpers.

---

## 🛠️ Tools & Environment
- **OS Used:** Ubuntu
- **Main Tools:** YARA CLI
- **Paths Used:** `~/yara-lab/rules/`, `~/yara-lab/samples/`

---

## 🔍 Enumeration / Setup

**Commands used**
```bash
yara myfirstrule.yar somefile
python3 loki.py -h
python ../../tools/Loki/loki.py -p
yara file2.yar file2/1ndex.php
```
---

## 📚 Key Takeaways
- 📌 Learned the structure of a YARA rule (**meta**, **strings**, **condition**).  
- ⚙️ Practiced running rules against files and specific directories.  
- 🛡️ Explored how **Loki** uses YARA rules for IOC detection.  
- 🔍 Reinforced YARA’s role in **malware detection and threat hunting**.  
