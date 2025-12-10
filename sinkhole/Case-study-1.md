
### The Worm No One Saw Coming 
One night, a student opens his laptop and realizes it’s acting up—slow, freezing, acting weird. He thinks, “Hmm, Windows being Windows…” The next morning, he sees the news on TV. He’s not alone. 15 million people worldwide have been infected by Conficker, a worm that spreads silently through unpatched machines and weak passwords.

The Conficker worm, discovered in November 2008 by Microsoft, silently infected unpatched Windows machines (2000, XP, Vista, Server 2003/2008) without any user action—no clicking links or opening emails. It spread automatically via the MS08-067 vulnerability, scanning networks and jumping from computer to computer. By April 1, 2009, a built-in trigger was set to scan remote sources for instructions, potentially giving attackers access to sensitive data from governments, banks, and other services. At its peak, Conficker infected an estimated **15 million PCs**, making it one of the fastest-spreading and most dangerous worms in history.

- **Infection:** Conficker spreads automatically by exploiting the **MS08-067 Windows vulnerability**, weak admin passwords, and removable media like USB drives—no user action required.
- **Botnet Integration:** Infected machines connect to attacker-controlled servers using a **Domain Generation Algorithm (DGA)** to receive commands and updates.
- **Command & Control:** The worm can download additional malware or instructions from these domains, and later variants included a **limited peer-to-peer update system** as a fallback.
- **Malicious Activities:** Conficker primarily propagates itself, scans networks, and maintains control over infected machines; it does **not steal money or lock files**.
- **Resilience:** The combination of DGA and P2P fallback makes Conficker **difficult to fully eradicate**, allowing it to persist for years.


### Extend Readings
- [Conficker Summary and Review](https://www.icann.org/en/system/files/files/conficker-summary-review-07may10-en.pdf)
- [A Look Back on the Conficker Worm](https://www.youtube.com/watch?v=dbL9g7ykfmc&t=127s)
