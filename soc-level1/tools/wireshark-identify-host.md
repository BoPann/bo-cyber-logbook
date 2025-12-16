## 1. Overview

When investigating an event, a SOC analyst needs persistent identifiers to link network activity to a physical machine and a user. 

Protocols that can be used in Host and User identification:
- Dynamic Host Configuration Protocol (DHCP) traffic
- NetBIOS (NBNS) traffic 
- Kerberos traffic

## 2. Description 
### 2.1 DHCP
- **MAC Address (Option 61):** This is the unique, physical address of the network card. It is the most reliable hardware identifier and is crucial for isolating the physical machine.
    
- **Hostname (Option 12):** The human-readable name of the machine (e.g., `FINANCE-PC07`). This is the ID used to search asset management systems and Endpoint Detection and Response (EDR) logs.

### 2.2 NetBIOS
- **NetBIOS Name:** NBNS queries and registration requests contain the NetBIOS name of the machine making the request. In many Windows environments, this name is the same as, or a truncated version of, the official hostname.
    
- **Service Information:** NetBIOS packets can also reveal the type of services running on the host (e.g., `<20>` for a server service, `<00>` for a workstation), which helps the analyst quickly profile the host's role on the network.

### 2.3 Kerberos
- **Client Name String (`CNameString`):** Kerberos Authentication Service Request (AS-REQ) packets contain the user ID attempting to log in or authenticate (e.g., `J.Doe`).
    
- **Service Principal Name (SPN) / Hostname:** Kerberos uses SPNs to identify services (and thus, the hosts they run on). An analyst can filter Kerberos traffic for values ending with a `$` (dollar sign) to often isolate the computer account name, which is the host's ID.