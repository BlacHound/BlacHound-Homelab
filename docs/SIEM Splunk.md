# SIEM Setup

It is time for me to choose a SIEM to montior network activity for my SOC team. 
I chose to go with Splunk Enterprise for the SIEM due to the company that I currently work for uses this and i;ve heard great things about it as being the industry standard for monitoring tool.

# What do I want Splunk to do.

- Collect logs of all host on the network
- Ingest logs from Sysmon, Windows Event Logs, Web servers, and the firewalls
- See the activity of all users and alert on critical threats.

I want to be able to see what a Soc Analyst see. I also want to know how can I harden the companies networks so it can remain free of any threat.

I will install sysmon on all hosts as well as DC01 (Domain Controller)

I will run external pentest to see if there are attacks that can go unnoticed un splunks survellance 

More to come on the capabilties and use cases of Splunk for now I just want to get it installed and forward logs from the Domain Controller to the SOC01 DC where Splunk lives.



<img width="2557" height="1382" alt="Splunk Enterprise Install and GitHub Documenting" src="https://github.com/user-attachments/assets/28394ad2-3642-44b9-b940-98bd68e6fed4" />



<img width="643" height="513" alt="Ingest DC01 Win Security Logs" src="https://github.com/user-attachments/assets/ee003941-66f6-4fd4-8d74-6e378fdf241f" />



<img width="1257" height="1142" alt="Screenshot 2026-02-25 214345" src="https://github.com/user-attachments/assets/78819899-1812-4b7e-9dd9-cd63e55de347" />


<img width="1277" height="1003" alt="Splunk Forwader working seeing login attempts" src="https://github.com/user-attachments/assets/2354b8e3-7a7b-4d3f-9361-818a14ba3749" />


<img width="1275" height="1159" alt="Building first detection rule" src="https://github.com/user-attachments/assets/c632de46-9623-4212-85bd-da7be9fca848" />


<img width="2541" height="1372" alt="T1059 001 – PowerShell" src="https://github.com/user-attachments/assets/0575f53c-9057-4c0a-9528-4a65f367da41" />
