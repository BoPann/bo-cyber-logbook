---
creation date: 2025-12-10 22:55
modified: 2025-12-10 22:55
tags:
  - cyber/atk
---

# Phishing 🎣

## 1. Overview
- how sending email work - [how-email-works](how-email-works.md)
- how to read email
- [types-of-phshing](types-of-phshing.md)

## 2. Description

### 2.1 Email Header 
- Received - the last hop before it reaches your email server (the is the _ONLY_ header that can be trusted, other fields can be [masqueraded](../masquerading.md))
- Return Path - the return email addr if the email fails to delivered
- X-Originating-ip - sender's ip 

### 2.2 DO NOT CLICK LINKS
- In fact, as SCO analyst, we should always "Defang" the email. Deganging means to **modify a potentially malicious indicator (like a URL or IP address) to make it non-functional and safe to share.** 
- [Defang Web](https://gchq.github.io/CyberChef/#recipe=Defang_URL(true,true,true,'Valid%20domains%20and%20full%20URLs')&input=aHR0cDovL3QudGVja2JlLmNvbQ&ieol=CRLF&oeol=CRLF)

### 2.3 BEC
- Business Email Compromise
- When the atker gains control of an internal employee's account and then uses the compromised email account to convince other internal employees to perform unauthorized or fraudulent actions.

## 3. Why it Matters?


## 4. Extended Readings
- [AoC Day2](advent-of-cyber-2025/day2-phishing.md)
- [Youtube: How Email Works?](https://www.youtube.com/watch?v=IMLFrYqI-oQ)
- [Understanding Email](https://web.archive.org/web/20221219232959/https://mediatemple.net/community/products/all/204643950/understanding-an-email-header)
- [Look Up the Sender IP](https://web.archive.org/web/20221219232959/https://mediatemple.net/community/products/all/204643950/understanding-an-email-header)