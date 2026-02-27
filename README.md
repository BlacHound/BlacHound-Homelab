# BlacHound-Homelab (SOC / Security Engineering Lab)

# This repo documents my end-to-end homelab build focused on:
- enterprise-style networking and segmentation
- Windows AD + GPO management
- central logging (Splunk)
- endpoint telemetry (Sysmon)
- detections mapped to MITRE ATT&CK
- incident simulations and response playbooks

## Lab Goals
- Build a realistic SOC test bench
- Practice detection engineering + investigations
- Practice secure architecture decisions (segmentation, least privilege, logging)

## What’s in the Lab
- pfSense (routing, VLANs, firewall rules, NAT)
- Windows Server (AD DS / DNS / GPO)
- SOC workstation/server (Splunk Enterprise)
- Windows endpoints + Sysmon telemetry
- Attack box (Kali) for controlled testing

## Repo Layout
- `/docs` → structured documentation (overview → architecture → detections)
- `/build-logs` → daily build journal
- `/challenges` → issues I hit + how I fixed them
- `/configs` → sanitized config examples + screenshots
- `/diagrams` → network diagrams (draw.io + PNG)

## Status
In progress. Current focus: Splunk ingestion + Sysmon + baseline detections.
