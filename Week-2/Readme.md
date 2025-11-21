# Week-2 SOC Analysis & Incident Response – Workflow  
Prepared by: Sahil Danecha  
Organization: CyArt  
Date: 21 Nov, 2025  

## 📌 Overview  
This folder contains all documentation, evidence, workflow steps, and reports completed for **Week-2 of the CyArt SOC Internship Program**.  
The tasks cover alert classification, incident response, evidence preservation, and a full exploitation-based investigation.

# 🧩 **Task 1 – Alert Classification & Prioritization**
### ✅ Steps Performed:
1. Performed port scanning on Metasploitable2 using Nmap (`-sS` scan).
2. Initiated Hydra SSH brute-force attack to generate authentication failures.
3. Sent HTTP probing traffic to the target using cURL.
4. Collected logs from:
   - Wazuh (if configured)
   - `/var/log/auth.log`
5. Classified alerts into:
   - Port scan detection  
   - SSH brute-force attack  
   - HTTP suspicious request  
6. Prioritized alerts using CVSS scoring & SOC severity levels.
7. Mapped alerts to MITRE ATT&CK techniques (e.g., T1110, T1190).

# 🧩 **Task 2 – Incident Ticketing & Escalation**
### ✅ Steps Performed:
1. Created an incident ticket for the SSH brute-force attack.
2. Documented:
   - Source IP (192.168.1.90)
   - Target IP (192.168.1.100)
   - Affected service: SSH (Port 22)
3. Drafted a professional escalation email to Tier-2 SOC team.
4. Added IOCs collected from logs.
5. Attached evidence screenshots.

# 🧩 **Task 3 – Incident Response Documentation**
### ✅ Steps Performed:
1. Investigated authentication logs (`/var/log/auth.log`) for brute-force evidence.
2. Reviewed login history using the `last` command.
3. Checked for unauthorized access indicators.
4. Built an incident timeline (Detection → Investigation → Findings).
5. Performed Root Cause Analysis (RCA).
6. Documented all steps with screenshots.

# 🧩 **Task 4 – Evidence Preservation**
### ✅ Steps Performed:
1. Captured active network connections using:
   - `netstat -tupan` (Kali + Metasploitable)
2. Identified active SSH processes using:
   - `ps aux | grep ssh`
3. Collected log files:
   - `/var/log/auth.log`
   - `/var/log/vsftpd.log`
4. Generated SHA256 hash for evidence integrity:
   - `sha256sum /tmp/auth.log`
5. Created a chain-of-custody table.
6. Stored all evidence files in the repository.

# 🧩 **Task 5 – Capstone: VSFTPD 2.3.4 Backdoor Exploit**
### ✅ Steps Performed:
1. Verified victim machine availability using `ping`.
2. Launched Metasploit:
3. Successfully gained a remote shell session.
4. Collected attacker-side evidence:
- Metasploit logs
- Command history (`history | tail`)
5. Collected victim-side logs:
- FTP connection logs
- Authentication logs
6. Created MITRE ATT&CK mapping (T1190).
7. Documented IOCs in a table.
8. Wrote:
- 200-word incident report  
- 100-word stakeholder briefing  
9. Included all screenshots in the Evidence Bundle.

# 📂 Repository Structure

cyart-soc-team/ │── Week 2/ │     ├── Week_2_Report.docx │              ├── Evidence/                         ├── Week2_Evidence_Bundle.docx │     ├── Screenshots/ │                    └── README.md (this file)

# 📝 Notes
- All screenshots and documentation were created manually during live attack simulations.
- This repository includes all evidence required for submission.
- All tasks follow CyArt SOC guidelines.

# ✅ End of README
