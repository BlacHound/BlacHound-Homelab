This lab was built to simulate a small enterprise for Blue Team, Red Team, and Security Engineering practice.

# Overview – Full Spectrum Cybersecurity Lab

This homelab is built to simulate a realistic enterprise environment for both offensive and defensive security operations.

The purpose of this lab is to:

- Simulate real-world attacks (Red Team)
- Detect and analyze those attacks (Blue Team)
- Continuously improve detections based on findings (Purple Team methodology)

This is a full adversary emulation and detection engineering test bench.

---

# Lab Objectives

## 🔴 Offensive Security (Red Team)

- Simulate internal and external attack scenarios
- Practice Active Directory enumeration and privilege escalation
- Execute controlled attacks from Kali against lab assets
- Test lateral movement techniques
- Simulate common MITRE ATT&CK techniques
- Validate exploit paths and misconfigurations
- Practice reporting and documentation like a real pentest

Goal: Understand how attacks work at a technical level.

---

## 🔵 Defensive Security (Blue Team)

- Centralize telemetry (Windows logs + Sysmon) into Splunk
- Build detections mapped to MITRE ATT&CK
- Create alert logic based on attacker behavior
- Perform log analysis and investigations
- Practice incident response workflow
- Validate segmentation and firewall rule effectiveness

Goal: Detect and respond to the attacks I simulate.

---

## 🟣 Purple Team Philosophy

Every attack simulation must produce:

1. Observable logs
2. Detection opportunities
3. A documented lesson
4. A refined detection rule

Attack → Observe → Detect → Improve → Repeat

---

# Architecture Philosophy

- Segment first, then deploy services
- Log everything before attacking
- Validate every change with testing
- Document all failures and troubleshooting steps
- Build detections based on behavior, not just signatures

---

# Core Technologies in the Lab

- pfSense (segmentation, routing, firewall rules)
- Windows Server (Active Directory, DNS, GPO)
- Windows endpoints (telemetry generation)
- Sysmon (process + network visibility)
- Splunk Enterprise (log ingestion + detection engineering)
- Kali Linux (controlled adversary simulation)
- VMware Workstation (virtualized infrastructure)

---

# Long-Term Goals

- Develop advanced detection engineering skills
- Map detections to MITRE ATT&CK techniques
- Practice red team tradecraft in a controlled environment
- Improve investigation speed and analytical thinking
- Build portfolio-ready documentation of real attack simulations

---

# Professional Focus

Primary specialization: Penetration Testing

This lab allows me to:
- Refine offensive techniques
- Understand detection blind spots
- Improve adversary emulation realism
- Strengthen reporting quality
- Think like both attacker and defender

This lab represents my commitment to mastering the full cybersecurity lifecycle.
