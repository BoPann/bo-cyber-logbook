---
creation date: 2025-12-26 10:58
modified: 2025-12-26 15:39
tags:
  - cyber/atk
  - cyber/articles
---
# SSH Brute Force 
source: [https://thehackernews.com/2025/04/outlaw-group-uses-ssh-brute-force-to.html#:~:text=Outlaw%20is%20a%20Linux%20malware%20that%20relies%20on%20SSH%20brute%2Dforce%20attacks](https://thehackernews.com/2025/04/outlaw-group-uses-ssh-brute-force-to.html#:~:text=Outlaw%20is%20a%20Linux%20malware%20that%20relies%20on%20SSH%20brute%2Dforce%20attacks)

# Article
Active [since at least late 2018](https://www.trendmicro.com/en_us/research/18/k/outlaw-group-distributes-botnet-for-cryptocurrency-mining-scanning-and-brute-force.html), the [hacking crew](https://www.countercraftsec.com/blog/dota3-malware-again-and-again/) has [brute-forced SSH servers](https://blogs.juniper.net/en-us/threat-research/dota3-is-your-internet-of-things-device-moonlighting), abusing the foothold to conduct reconnaissance and maintain persistence on the compromised hosts by adding their own SSH keys to the "authorized_keys" file.

## Thoughts
Pretty alarming. This shows that even a secure encrypted connection can be compromised if the user’s credentials are weak.
1. **Stop using passwords.** Use key-based authentication instead—keys don’t get brute-forced easily. 
2.  **Use Fail2Ban.** When too many failed login attempts are detected, we should politely shows attackers the door (by banning their IP). 🫸

>last modified: 2025-12-26