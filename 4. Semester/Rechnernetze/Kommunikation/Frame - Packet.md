
# Frame
 An Ethernet Frame refers to a data unit at the [[Schichtenmodell#2. Data Link|Data Link]] Layer 
- It is used to transmit data across a **single physical Network** (LAN)
- Processed by [[Switches]] or [[Bridges]]
## Aufbau
- **Preamble**: A sequence of bits used for synchronization (not always counted in the frame itself).
- **Start of Frame Delimiter** (*SFD*): feste Bitfolge zur Identifikation des Frame-Anfangs (1 Byte)
- **Destination MAC Address**: The 6-byte address of the receiving device.
- **Source MAC Address**: The 6-byte address of the sending device.
- **EtherType/Length**: Indicates the protocol type (e.g., IPv4, IPv6) or the length of the payload.
- **Payload/Data**: The actual data being transmitted (46–1500 bytes).
- **Frame Check Sequence (FCS)**: A 4-byte cyclic redundancy check (CRC) for error detection.

## Minimale Länge 
Packetlänge darf nicht eine bestimmte Länge **unterschreiten**, um Kollisionen in einem Medium zuverlässig erkennen zu können (mit [[CSMA - CD]])
- So wird es sichergestellt, dass eine Frame lang genug ist, damit eine **Kollision während der gesamten Sendezeit erkannt werden** kann
### Round Trip Zeit
Ein Frame wird mindestens so Lange übertragen, wie ein Signal die maximale Strecke in der Netzwerk benötigt (**hin und züruck**)
- So kann der Sender eine Kollision erkennen bevor das Frame vollständig geschickt würde
![[Pasted image 20250502160030.png]]
---

# Packet
Operates at the [[Schichtenmodell#3. Network | 3. Network Layer]] 
- Used to transmit **Data across different Networks** 
- Processed by routers or gateways 
## Composition 
 Relies on the IP for routing 
 - **Destination and Source IP Addresses** (4 bytes each for IPv4, 16 bytes for IPv6).
- **Protocol** (e.g., TCP, UDP).
- **Payload** (data or higher-layer protocol like TCP/UDP segments)