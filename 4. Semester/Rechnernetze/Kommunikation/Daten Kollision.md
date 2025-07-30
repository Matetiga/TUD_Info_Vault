Beim Senden von Daten über einem Medium, können sie **miteinander kollidieren** *falls zwei Benutzer gleichseitig Pakets schicken*

Jede benutzer kann über dem Kanal mithören und bemerken ob es frei ist, bzw. ob Kollisionen entstehen 

--- 

## Pure ALOHA
>[!Use]
>Used in situations where devices share a common communication channel

This protocol **allows devices to transmit data at any time**, without a set schedule. 
- This is known as a *random access technique*, and it is **asynchronous** because there is **no coordination** between devices. 
- When multiple devices attempt to transmit data at the same time, it can **result in a collision**, where the data becomes garbled.
	- In this case, each device **will simply wait a random amount of time** before attempting to transmit again.

### Kollisionen
Entstehen beim Empfänger, aber Sender muss sie erkennen, um die Packeten wieder zu schicken
- Nach der Entdeckung von einem Kollision wird ein JAM-Packet geschickt (Sender hört mit un erkennt Kollision)

---

## Slotted ALOHA 
Sendevorgang startet nur zu Beginn eines Taktslots
- Dabei muss jeder Benutzer synchroniziert mit den anderen Computern sein, um daten mit demselben Takt zu schicken 


---
## Übersicht
- [[CSMA - CD]]
![[Pasted image 20250424120937.png]]