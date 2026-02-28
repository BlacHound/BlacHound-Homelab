🔐 OFFICIAL HOMELAB MASTER RECORD

1️⃣ Core Architecture
pfSense Interfaces
Zone	Interface	IP	Subnet
WAN	em0	192.168.154.128	/24
CORP_LAN	em1	10.0.0.1	10.0.0.0/24
SOC_NET	em3	10.0.1.1	10.0.1.0/24
ATTACKER_NET	em2	10.0.3.1	10.0.3.0/24
2️⃣ Identity Layer
DC01

Hostname: DC01

Domain: corp.local

Role: AD DS + DNS

IP: 10.0.0.10

Gateway: 10.0.0.1

DNS: Self (10.0.0.10)

Netlogon: Running

SRV Records: Present

3️⃣ Corporate Workstation
DESKTOP-94T0BP0

Domain joined: corp.local

IP: 10.0.0.100 (DHCP)

Gateway: 10.0.0.1

DNS: 10.0.0.10

DHCP Server: 10.0.0.10 (DC01)

✔ DHCP running from DC01
✔ CORP_LAN clients use AD DNS

4️⃣ SOC Layer
SOC01

IP: 10.0.1.10

Gateway: 10.0.1.1

DNS: 10.0.0.10

Splunk Enterprise Installed

Splunk receiving on port 9997

Windows firewall rule created for 9997

Sysmon installed

EventCode=1 confirmed indexing

SOC_NET Firewall Rules:

DNS → 10.0.0.10 (53)

Kerberos → 88

LDAP → 389

SMB → 445

RPC → 135

RPC High Ports → 49152–65535

NTP → 123

ICMP allowed

Internet allowed

Segmentation preserved.

5️⃣ Attack Layer
Kali

IP: 10.0.3.50

Subnet: 10.0.3.0/24

Gateway: 10.0.3.1

No direct access to CORP_LAN

No direct access to SOC_NET

Internet allowed

ATTACKER_NET Firewall Rules:

Block → CORP_LAN

Block → SOC_NET

Allow → Internet

ICMP → pfSense

This is proper red segmentation.

6️⃣ Firewall Policy Summary
CORP_LAN

Block to ATTACKER_NET

Allow to SOC_NET (AD return traffic)

Default allow LAN → any (internal)

SOC_NET

Allow AD-specific ports to DC01 only

Allow Internet

ICMP allowed

No broad access to CORP_LAN

ATTACKER_NET

Explicitly blocked to CORP_LAN

Explicitly blocked to SOC_NET

Internet only

7️⃣ Telemetry Flow

Attack Surface → Domain → DC logs
DC logs → SOC01 via Splunk Forwarder
SOC01 indexes → searchable
Sysmon operational → working

You now have a full Red → Blue detection loop foundation.

🧠 Important Architectural Observations

✔ Segmentation is correct
✔ AD isolation is correct
✔ SOC isolation is correct
✔ Attacker isolation is correct
✔ Telemetry path confirmed
✔ DHCP centralized on DC01
✔ DNS centralized on DC01

This is structured like a small enterprise.
