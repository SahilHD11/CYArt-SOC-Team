# Week 4 – SOC Operations & Incident Response (Tasks 1–8)

---

# 📁 Repository Structure
.
├── Week_4_Report.docx
└── README.md

---

# 📌 Included Tasks

1. **Advanced Log Analysis (Filebeat + Elastic)**  
2. **SOAR Playbook Development (IP Reputation + Auto-Block)**  
3. **Post-Incident Analysis (5-Whys + Fishbone)**  
4. **Alert Triage & Automated Malware Validation**  
5. **Evidence Handling & Chain of Custody**  
6. **Adversary Emulation (Caldera – MITRE TTP Simulation)**  
7. **Security Metrics & Dashboarding (MTTD/MTTR)**  
8. **Capstone Attack Simulation (Metasploit → Wazuh → TheHive → CrowdSec)**  

---

# 🔄 **SOC WORKFLOWS**

Below are the operational workflows used during Week-4.  
These diagrams represent real SOC processes and can be used in documentation or interviews.

---

# 1️⃣ **Log Collection & Ingestion Workflow**

+------------+ +-----------+ +----------------+ +-------------+
| Endpoints | ---> | Filebeat | ---> | Elasticsearch | ---> | Kibana SIEM|
| (Linux/Win)| | (Ship) | | (Index/Store) | | Dashboards |
+------------+ +-----------+ +----------------+ +-------------+

---

# 2️⃣ **Detection → Triage → Containment Workflow**

Suspicious Event
|
v
+----------------+
| Wazuh Rule Hit |
+----------------+
|
v
+----------------------+
| SOC Analyst Triage |
+----------------------+
|
+---- Benign → Close Ticket
|
+---- Malicious →
|
v
+-----------------------+
| Containment (Block IP |
| Isolate Host, etc.) |
+-----------------------+

---

# 3️⃣ **SOAR Automation Workflow (Task 2)**

Incoming IOC (IP/Hash)
|
v
+------------------------+
| Threat Intel Lookup |
| (VT, OTX, AbuseIPDB) |
+------------------------+
|
Malicious? (Yes/No)
|
+-----+-----+
| |
Yes No
| |
v v
+--------------------+ +------------------+
| Auto Block (FW/CS) | | Close as Clean |
+--------------------+ +------------------+

---

# 4️⃣ **Evidence Handling Workflow (Task 5)**

Evidence Collected
|
v
+----------------------+
| Verify Integrity |
| (Hash SHA256) |
+----------------------+
|
v
+----------------------+
| Store in Evidence DB |
+----------------------+
|
v
+----------------------+
| Analysis + Reporting |
+----------------------+

---

# 5️⃣ **Capstone Attack Simulation Workflow (Task 8)**

Attacker (Kali)
|
v
Exploit Samba (T1210)
|
v
+-----------------------+
| Wazuh Detection |
+-----------------------+
|
v
+-----------------------+
| SIEM Investigation |
+-----------------------+
|
v
+-----------------------+
| TheHive Case Creation |
+-----------------------+
|
v
+-----------------------+
| CrowdSec Auto-Block |
+-----------------------+

---

# ⭐ Key Highlights

- Full end-to-end SOC workflow demonstrated  
- Realistic Metasploit attack simulation  
- Automated IP reputation and containment logic  
- Detailed RCA & professional reporting  
- Dashboarding for MTTD, MTTR, alert frequency  
- Evidence handling using forensic standards  

---

# 🛠 Tools Used

- Elastic Stack (Filebeat, Elasticsearch, Kibana)  
- Wazuh SIEM  
- TheHive SOAR  
- CrowdSec IPS / UFW Firewall 
- Metasploit Framework  
- Velociraptor  
- MITRE Caldera (Adversary Emulation)  
- GeoIP & Threat Intel APIs  

---

# 🧾 Author
Sahil Danecha

---

