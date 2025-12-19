---
creation date: 2025-12-15 19:28
modified: 2025-12-18 13:04
tags:
---
# FTP
FTP is always sent in clear text!

File Transfer Protocol (FTP) is designed to transfer files with ease, so it focuses on simplicity rather than security. As a result of this, using this protocol in unsecured environments could create security issues like: 
- MITM attacks
- Credential stealing and unauthorised access
- Phishing
- Malware planting
- Data exfiltration

### 1. The Control Channel (Command Channel)

- **Port:** Typically **TCP Port 21**.
- **What it is:** This is where the "conversation" happens. The client sends commands like `USER`, `PASS`, `LIST` (to see files), and `RETR` (to retrieve/download a file). The server sends back status codes (e.g., `230 Login successful`).
- **SOC Use:** You isolate this to find **Who** is logging in, **What** commands they are running, and **Where** they are trying to go.
### 2. The Data Channel

- **Port:** Typically **TCP Port 20** (in Active mode) or a **Random High Port** (in Passive mode).
- **What it is:** This channel is created only when a file is actually being transferred or a directory list is being sent. It carries the raw bytes of the file itself.
- **SOC Use:** You isolate this to see **How much** data was moved and to **reconstruct the file** for malware analysis or to check for data exfiltration.


### So who's still using FTP?
Sending data in plain text is a massive security risk. In a modern SOC, seeing standard FTP (Port 21) usually triggers an immediate alert because credentials and data are "in the clear." However, it is still surprisingly common in certain environments.

1. Legacy System - they are old and people tend to not bother change them
2. Internal Network - In some organizations, IT teams might use FTP for moving non-sensitive files (like printer drivers or public documentation) between internal servers, assuming that since it's "behind the firewall," it is safe.

>last modified: 2025-12-18 