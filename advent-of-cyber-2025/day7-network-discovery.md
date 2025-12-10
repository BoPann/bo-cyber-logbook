---
creation date: 2025-12-07 23:52
modified: 2025-12-09 13:29
tags:
  - cyber/networking
---
## Overview
>A port is like a doorway that a service uses on a machine.  
If a port is left open by accident, it can make the system easier to attack.  
This exercise shows how an open port can be used by an attacker if the service behind it is not secure. It's been seven fun days! 

## Decription
1. nmap to scan the network 
2. use different command to connect to open port
	1. ftp to interact with the ftp server
	2. nc to interact with network service
	3. dig to query the dns server
3. By this time we have all the flag to log in to the http server
4. Lasly when we are in, we can run `ss -tunlp` to see all the open port of the system!

## Why this Matters?
As a hacker, we want to be able to discover the potential targets. As a SOC analyst, we want to be able to identify the vulnerable devices on the network. Scanning is a important part of that. 