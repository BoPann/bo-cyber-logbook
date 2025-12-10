---
creation date: 2025-12-09 15:07
modified: 2025-12-09 15:29
tags:
  - cyber/atk
---
## 1. Overview


## 2. Description
### 2.1 Types of atks
>Before running the atks, we need to first figure out the type of the file `file fileName`
- dictionary atk 
	- having a wordlist and go thru them
- mask atk
	- specify the format of the password (if known). This can reduce the time for brute forcing. 
### 2.2 Tools available
- PDF: `pdfcrack`, `john` (via `pdf2john`)
- ZIP: `fcrackzip`, `john` (via `zip2john`) John can not crack zipfile. We need t convert the zip to a hash first!
- General: `john` (very flexible) and `hashcat` (GPU acceleration, more advanced)
### 2.3 How to detect?
- if someone tried to download/use those tools or wordlist, he/she might be suspecious
- if an high surge of GPU/CPU usage is obaserved, an investigation should be conducted.

## 3. Why it Matters?
- As a hacker, cracking file password should be a basic skills. As a SOC analyst, we should be able to detect the attacks based on the data gather from SIME tools. 

## 4. Extended Readings
