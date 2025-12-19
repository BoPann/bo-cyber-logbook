# MITM Detection


### MITM
Man-In-The-Middle attacks is when the bad actor place itself between 2 ends of the communication. He can intercept packets, and potentially (very likely) steal crenditial or valuable information and even temper with the communication. To achive this, a bad actor typically needs 1. sniffing(capture) 2. spoofing(redirect) the traffic. 

- Packet sniffing: Capturing unencrypted data packets exchanged over a network, often on open Wi-Fi.
- Session hijacking: Stealing and using session tokens to impersonate users.
- SSL stripping: Downgrading HTTPS connections to insecure HTTP to steal or alter data transferred.
- DNS spoofing: Redirecting legitimate website traffic to fraudulent domains by manipulating DNS responses.
- IP spoofing: Crafting malicious IP packets that appear to come from trusted systems.
- Rogue Wi-Fi access point: Creating fake networks to intercept user traffic.

### ARP Spoofing
- the attacker send out `is-at`message (typically the router ip) and to whoever sending the arp reuest. (ARP has no authentication, which is vulnerable)
- Indicator
	- duplicate mac-ip mappings
	- huge number of arp replied (code 2) without matching request (gratuitous reply)

### DNS Spoofing
- DNS is  the fundamental that powers internet. It is a phone book that tells us where to go(ip) with the given domain name. Without it, the computer will not be able to pull the information we want. However, attacker can imporsonate the DNS Server and spoofing as the ligit one. 
- Indicator
	- looks for response that does not come from a DNS server (i.e, 8.8.8.8)

### SSL Striping
- HTTPS encrypt message and prevent the bad actors from looking at the content. However, when a MITM is performed, the bad actors can intecept the message and replay the message to the victim with HTTP. 
- When we can identify who the middle man is, we can confirm with by search the ip with the http request. 



## Extended Reading
- [Bo Cyber Logbook - Wireshark](../tools/wireshark.md)