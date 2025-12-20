# Industrial Control

### SCADA (Supervisory Control and Data Acquisition)
- sensors and actuators
- PLC (decesion maker)
- monitoring system
- historians (log)

### SCADA often targeted becasue: 
- They often run **legacy software** with known vulnerabilities. Many SCADA systems were installed decades ago and never updated. Security patches that exist for modern software don't exist for these ageing systems.
- **Default credentials** are commonly left unchanged. Administrators prioritise keeping systems running over changing passwords. In industrial environments, the mentality is often "if it works, don't touch it"—a recipe for security disasters.
- They're designed for **reliability, not security**. Most SCADA systems were built before cyber security was a significant concern. They were intended for closed networks that were presumed safe. Authentication, encryption, and access controls were afterthoughts at best.
- They control **physical processes**. Unlike attacking a website or stealing data, compromising SCADA systems has real-world consequences. Attackers can cause blackouts, contaminate water supplies, or—in our case—sabotage Christmas deliveries.
- They're often **connected to corporate networks**. The myth of "air-gapped" industrial systems is largely fiction. Most SCADA systems connect to business networks for reporting, remote management, and data integration. This connectivity provides attackers with entry points.
- Protocols like **Modbus lack authentication**. Many industrial protocols were designed for trusted environments. Anyone who can reach the Modbus port (502) can read and write values without proving their identity.

### SCADA Components
- PLC - the motherboard
- Modbus - the communication protocol that industrial devices use to talk to each other. (client-server communication)
	
