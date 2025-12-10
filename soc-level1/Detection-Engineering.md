# Dectection Engineering
## Goal 
Detection engineering is the continuous process of building and operating threat intelligence analytics to identify potentially malicious activity or misconfigurations that may affect your environment. 

## 2 Approaches
1. Env-based
	- configuration detection
	- modelling (build a asset or activity profile for baseline events)
2. Threat-based
	- indicators
	- threat behavior detections

## Framework
- [MITRE](MITRE.md)
	- MITRE ATT&CK - shows what attackers usually do in the real world. see [official MITRE ATT&CK Doc](https://attack.mitre.org/matrices/enterprise/)
	- MITRE CAR - In contrast to ATT&CK, it shows how to catch them! see [official MITRE CAR Doc](https://car.mitre.org/analytics/)

- Pyramid of Pain - how difficult it is for attackers when defenders block different types of indicators. see [Pyramid-of-Pain](Pyramid-of-Pain.md)
- Cyber Kill Chain - the steps that cyber attacks commonly follow. It then be developed into  [Unified Kill Chain](unified-kill-chain.md) which covers 18 phases. see [Official Cyber Kill Chain Doc](https://www.unifiedkillchain.com/assets/The-Unified-Kill-Chain.pdf)
	- Reconnaissance
	- Weaponisation
	- Delivery
	- Exploitation
	- Installation
	- Command & Control
	- Actions on Objectives
- ADS - Alerting and Detection Strategy. The ADS Framework has a strict flow that detection engineers must follow before publishing detection rules into production. see [ADS Official Doc](https://github.com/palantir/alerting-detection-strategy-framework)
- DML - Detection Maturity Level Model. A framework for organizations  to evaluate their security level. 