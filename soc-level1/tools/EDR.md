# EDR
Endpoint Detection and Response (EDR) is a security solution designed to monitor, detect, and respond to advanced threats at the `endpoint level`.

To ensure these endpoint devices are protected even out of the network, we need a security solution that guards all devices in different areas and is capable of fighting advanced threats. Endpoint Detection and Response (EDR) is a security solution that offers deep-level protection for endpoints. No matter where the endpoints are, the EDR will make sure they are monitored constantly and threats are detected.

## Process
In computing, a process is an instance of a program that is being executed. It contains the program code and its current activity, including the program counter, registers, and variables. Each process has its own memory space and system resources. 

## How does Process help in SOC?
Processes are crucial in a Security Operations Center (SOC) as they help monitor, detect, and respond to security incidents. By analyzing processes running on endpoints, SOC teams can identify malicious activities, like unauthorized access or malware execution. Understanding processes allows for better threat hunting and incident response, ultimately enhancing the organization's security posture.


## Antivirus vs EDR 
- Antivirus is like an immigration check. It check the passports of people when they pass through immigration. The immigration check (AV) monitors incoming people and matches their passports with a list of known criminals in its database. If there is a match, the entry is blocked and caught.

>But, what happens if somebody who has never been identified as a criminal in the past and has an innocent personality tries to come in?

- EDR is like the security offices. They constantly monitor the security cameras and motion sensors in the airport (endpoint). 

>Both solution are important to make sure the airport is safe from threats!


## Roles of EDR 
- endpoint aka agent aka censor
- central (monitor all endpoints)
- the data sent from agents to central is called `telemetry`

## what EDR does?
- detect (based on behavior, anomaly, indicator of compromising aka ioc matching...)
- response (isolation, termination, quauratine...)

