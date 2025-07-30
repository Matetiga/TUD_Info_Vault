### Use 
- to prevent loops inside a network Topology
- Loops can arise when devices share Data over the same LAN

## Segmented LAN
A segmented LAN is often designed with **redundant bridges** and paths to ensure that communications can continue in the event that a network link becomes unavailable
- This makes the network more susceptible to looping

When STP is enabled, each [[4. Semester/Rechnernetze/Bridges/Bridge|Bridge]] learns which computers are on which segment by sending a first-time message to network segments.


---

## Protocol 
**root ID | cost | bridge ID | port ID**

### Steps
1. *Root tree* (<span style="color:#ffff00">switch with lowest ID</span>) is selected within the Switches of the same Network before the **STP-Algorithm** is ran  
	- Root is responsible for sending configuration *Bridge Protocol Data Units* (BPDUs) 
	- Each Bridge has its ID (**BID**) and a *combination* of their **priority value** with the switch's **MAC-Address**
	- If a Bridge receives a packet from the root, it sends the transition costs back
2. Designiere ein Switch pro LAN fest (Switch der am dichsten zur Wurzel ist)
3. Bestimme den Ports zu Wurzel 
	- The port with the lowest root path is selected as the root port
	- If the path cost is the same, the switch will select the port with the lowest sender BID as the selected root port