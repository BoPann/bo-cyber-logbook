## Overview
The attacker will try to scan netowrk inlcuding the ip, ports, services, etc... 
reconnaissance: SOC can observe external ip to internal ip 
discovery: the attacker got in. The SOC can see internal ip scaning internal ip

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