---
creation date: 2025-12-05 09:45
modified: 2025-12-09 13:35
tags:
  - cyber/atk
---
## Overview
Think about you walk in to a bank and go strait into the vault where all the money are stored. That easy? You think. It will be if no one was check along the way. 

## Description
>This is also known as Broken Access Control. This is on top of the most severe web app security risk by OWASP

### Insecure Direct Object Reference (IDOR)
That’s when an app basically says, “Sure, help yourself,” and hands a user data they should _definitely_ not be seeing.
### Solution  
Add proper authorization. In other words, make sure the app asks, “Hey, is this actually your stuff?” before giving anything away.

## Why this Matters
As a hacker, this is great! We can steal valuable assets easily. As a SOC analyst, we need to address this immeditely as this can cause the company a fortunate!