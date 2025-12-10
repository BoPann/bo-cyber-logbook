
### You know what people like doing? Clicking links!
Early one morning, a woman checks her email and finds an urgent message claiming her package couldn’t be delivered. She clicks the link without thinking. GOZ installs instantly, joining a hidden P2P botnet that quietly steals her banking logins. Later that day, she opens her banking app and sees her balance is zero—her money was drained through accounts controlled by cybercriminals. At the same time, another victim across town discovers all his files locked by the botnet’s ransomware partner. Both were hit by a single click.


- **Infection:** GOZ primarily spreads through **phishing emails**, malicious attachments, or drive-by downloads.
- **Botnet Integration:** Once a computer is infected, it joins the **peer-to-peer (P2P) botnet**, communicating with other infected machines instead of a central server.
- **Command & Control:** Instructions, updates, and additional malware are sent through the P2P network or, as a fallback, via **DGA-generated domains**.
- **Malicious Activities:** GOZ steals banking credentials, initiates unauthorized transfers, and can deliver other malware, such as **ransomware**.
- **Resilience:** The P2P structure and DGA fallback make GOZ **hard to disrupt**, allowing it to operate even if some nodes are taken down.

### Extended Readings
- [Highly resilient peer-to-peer botnets are here: An analysis of Gameover Zeus](https://ieeexplore-ieee-org.seattleu.idm.oclc.org/document/6703693/references#references)
- [SoK: P2PWNED - Modeling and Evaluating the Resilience of Peer-to-Peer Botnets](https://ieeexplore-ieee-org.seattleu.idm.oclc.org/document/6547104/footnotes#footnotes-id-fn3)