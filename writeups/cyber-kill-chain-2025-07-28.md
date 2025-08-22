# 🔒 TryHackMe — Cyber Kill Chain

## 🧾 Lab Info
- **Room Name:** Cyber Kill Chain
- **Difficulty:** Easy
- **Category:** Cyber Defence Frameworks
- **Date Completed:** 2025-07-28

---

## 🎯 Objectives
- Understand the **Lockheed Martin Cyber Kill Chain** model.
- Learn how attackers move through phases of an intrusion.
- Map defensive strategies to each stage.
- Relate the framework to real-world SOC workflows.

---

## 🛠️ Tools & Environment
- **OS Used:** Ubuntu (VM)  
- **Main Tools:** Browser-based lab environment (TryHackMe portal)  
- **No external tools required**  

---

## 📚 Framework Breakdown

**Cyber Kill Chain Phases**
1. **Reconnaissance** – Gathering information about targets (OSINT, scanning).  
2. **Weaponization** – Crafting malicious payloads (e.g., malware, exploit).  
3. **Delivery** – Transmitting payload (email, USB, watering hole).  
4. **Exploitation** – Triggering the vulnerability.  
5. **Installation** – Establishing persistence (backdoors, trojans).  
6. **Command & Control (C2)** – Attacker communicates with compromised system.  
7. **Actions on Objectives** – Data exfiltration, sabotage, lateral movement.  

---

## 🔍 Defensive Mapping

- **Reconnaissance** → Monitoring OSINT, threat intel feeds, web logs.  
- **Weaponization** → Difficult to detect; rely on **threat intel + malware sandboxing**.  
- **Delivery** → Block via **email filters, firewalls, IDS/IPS**.  
- **Exploitation** → Mitigate with **patching, vulnerability management**.  
- **Installation** → Detect persistence with **endpoint protection + EDR tools**.  
- **C2** → Block/detect anomalous outbound traffic with **network monitoring**.  
- **Actions on Objectives** → Prevent lateral movement via **segmentation, least privilege, monitoring**.  

---

## 📈 Key Takeaways
- The Cyber Kill Chain breaks down attacks into predictable steps.  
- Mapping defense to each stage gives analysts a proactive approach.  
- **Weakest phases for defenders:** Recon & Weaponization (hard to spot).  
- **Strongest phases for defenders:** Delivery, C2, and Actions (more visibility).  
- Real SOCs often extend this model with **MITRE ATT&CK** for more detailed tactics/techniques.  

---
