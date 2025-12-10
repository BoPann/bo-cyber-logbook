`The solution is twofold`
### Global Domain Pre-registration (Sinkholing at the source)

- Conficker’s DGA generates thousands of domains every day.

- Security teams (Conficker Working Group) pre-registered these domains before the malware tried to use them.

- This ensures that any infected machine trying to resolve a DGA domain hits a safe sinkhole server instead of the real C2.

### Local DNS Blocking

- Organizations or home users can run a DNS filter

- Any request for known malicious domains (from blocklists or observed DGA domains) is intercepted locally and redirected to a safe address or blocked.


### It's worth to note (but out of scope of this presentation):
1. **Conficker evolved into P2P variants** – Later versions of Conficker adopted a peer-to-peer structure, allowing infected machines to share updates directly, making the botnet more resilient even when domain-based C2 channels were blocked.
    
2. **Gameover Zeus (GOZ) uses a more resilient P2P structure** – GOZ bots primarily connect to peers for commands. If peers are unresponsive, the bots fall back to connecting to hardcoded domain servers. To disrupt GOZ, researchers developed a two-step strategy: 
    
    1. **Partitioning** – Break enough connections in the P2P network to split the botnet into isolated components, preventing commands from spreading.
        
    2. **Sinkholing** – Rewrite bots’ neighbor lists so most or all point to defender-controlled “sinkholes,” effectively hijacking the botnet’s communication layer.

Resource (how to take down p2p): [SoK: P2PWNED - Modeling and Evaluating the Resilience of Peer-to-Peer Botnets](https://ieeexplore-ieee-org.seattleu.idm.oclc.org/document/6547104/footnotes#footnotes-id-fn3)
        

> This combination of partitioning and sinkholing allowed defenders to neutralize GOZ despite its decentralized P2P design.
