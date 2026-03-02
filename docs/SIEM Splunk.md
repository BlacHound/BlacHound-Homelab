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
