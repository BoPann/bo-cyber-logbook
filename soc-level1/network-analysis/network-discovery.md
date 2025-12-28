---
creation date: 2025-12-17 11:24
modified: 2025-12-27 16:37
tags:
  - cyber/atk
  - cyber/networking
---
# Network Discovery
So, you're telling me one guy is knocking on the front door, the back door, the windows, _and_ the chimney? **Could he BE any more suspicious?** 
## Overview
Netowork Discovery is like asking "Hello? Is any body here?" \
In Cybersecurity, the attackers will try to scan netowrk inlcuding the ip, ports, services, etc... This can happen is [cyber-kill-chain](../framework/cyber-kill-chain.md) reconnaissance and discovery. 
- Reconnaissance: SOC can observe external ip to internal ip 
- Discovery: the attacker got in. The SOC can see internal ip scaning internal ip

## Description
In scanning, typically we can see a massive amount of packets, including ICMP, TCP, UDP from the same IP address. That should ring the bell when it happens ... someone is looking for victims!

### Scan Types
- horizontal scanning - scanning multiple internal ips
- vertical scanning - scanning same ip but multiple ports

- Ping Sweep
	- ICMP packet
	- often blocked

- TCP Syn Scans
	- harder to detect 

- UDP Scans
	- slow and unreliable 

## Extended Readings
- [Bo Cyber Logbook - Log Analysis](log-analysis.md)
- [Bo Cyber Logbook - Kibana](../tools/Kibana.md)

---
Last Modified: 2025-12-27  \
Have Questions? Shoot me a text >> [Linkedin](https://www.linkedin.com/in/bopann/)


