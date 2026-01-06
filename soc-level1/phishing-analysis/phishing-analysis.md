---
creation date: 2025-12-11 12:06
modified: 2025-12-12 21:54
tags:
  - cyber/dfd
---

# Phishing Analysis
Have you been phished?

## 1. Overview
- Do not click any link!!!
- Check header
	- `Received` - the last hop before it reaches your email server (the is the _ONLY_ header that can be trusted, other fields can be [masqueraded](../atks/masquerading.md))
	- `Return Path` - the return email addr if the email fails to delivered
	- `Replay-To` - The addr when users hit reply
	- `X-Originating-ip` - sender's ip 
	- **The Bottom-Up Rule:** Read them from bottom to top. The top-most is the last server receiving it.
	- `Authentication-Results` - does it pass SPF, DKIM, DMARC?

- Check body in source code
	- Attackers often hide malicious code in the HTML/CSS (like transparent text or hidden redirects) that you can't see in the regular preview.
- Usually there is link, check the link source
	- has it been shortened? see: [Bo Cyber Logbook - Shortened Url](../atks/shortened-url.md)
	- A link might say `portal.microsoft.com` but the source code reveals it points to `evilhacker.ru/login`.

## 2. Description

### 2.1 DO NOT CLICK LINKS (Have I said that already?)
- In fact, as SCO analyst, we should always "Defang" the email. Deganging means to **modify a potentially malicious indicator (like a URL or IP address) to make it non-functional and safe to share.** 
- [Defang Web](https://gchq.github.io/CyberChef/#recipe=Defang_URL(true,true,true,'Valid%20domains%20and%20full%20URLs')&input=aHR0cDovL3QudGVja2JlLmNvbQ&ieol=CRLF&oeol=CRLF)

### 2.2 Some Common Tactics
- **Spoofed email address**
- **URL shortening services**
- **HTML to impersonate a legitimate brand**
- **Pixel tracking**. See [Bo Cyber Logbook - Pixel Tracking](../atks/pixel-tracking.md)
* Link manipulation
* Credential harvesting - [example on anyrun](https://app.any.run/tasks/12dcbc54-be0f-4250-b6c1-94d548816e5c/)
* typosquatting - see [Bo Cyber Logbook - Typosquatting](../atks/typosquatting.md)


### 2.3 Tools of Trade
Here are some tools that come in handy for analyzing email. They are also useful tools in general too!

- Header Analysis
	- https://toolbox.googleapps.com/apps/messageheader/analyzeheader
	- https://mha.azurewebsites.net/
	- https://mailheader.org/
- Extracting link is tedious, here are some tools to help with that (thank god)
	- https://www.convertcsv.com/url-extractor.htm
	- https://gchq.github.io/CyberChef/#recipe=Extract_URLs(false,false,false)
- PDF Parser
- Threat Intel including website, domain, ip and file - [Bo Cyber Logbook - Threat Intelligence](../threat-intelligence.md)


## Extended Readings: 
- [Bo Cyber Logbook - Threat Intelligence](../threat-intelligence.md)



---
last modified: 2026-01-02