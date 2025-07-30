## User Datagram Protocol 
Bei ausschließlich Portbasierte Kommunikation gibt es folgende Probleme:
- Keine Sicherstellung ob Packet wirklich gekommen ist 
- Keine Sicherstellung der Packeten Reihenfolge
- Fehlerbehandlung 
- Keine Flusskontrolle 
- **Verbindungslos** (also es baut keine dauerhafte Verbindung zwischen Sender und Empfänger)
	- Bei TCP wäre es die [[Drei Wege Handshake]]
### Vergleich mit [[4. Semester/Rechnernetze/Transportschicht/TCP|TCP]]
![[Pasted image 20250701110902.png]]


## UCP statt TCP 
- UCP hat einen *kleineren Header* 
- UCP hat *weniger Latenz*, da kein Verbindungsaufbau/ -abbau gemacht werden muss 