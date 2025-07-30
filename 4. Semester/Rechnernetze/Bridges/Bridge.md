## Use
Um zwei LAN-Segmente zu verbinden 
- Forwards [[Frame - Packet#Frame|Frames]] in a LAN based on the MAC-Address
- Can operate in different Modes: [[Transparent Bridges]], source-route or translational

### When [[Spanning tree Protocol]] is active
When STP is enabled, each bridge learns which computers are on which segment by sending a first-time message to network segments.
- When subsequent messages are sent, the bridge uses the table to determine which segment to forward them to.

---
## Forwarding Tabelle 
<MAC-ADDRESS, port, age> 
- [[Switches#MAC-Address|MAC-Address]]
- **port**: port number of bridge used to send data to the host 
- **age**: aging time of entry (optional)
Hier werden Sender von Packeten eingetragen, so werden mögliche Empfänger von Packeten gelernt 