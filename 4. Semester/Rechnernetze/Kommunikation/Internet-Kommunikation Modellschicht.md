## Schichten 
1. **Physical**
	- Die physikalische Schicht stellt sicher, dass **Datenpakete korrekt über ein physisches Medium**, beispielsweise ein *Kabel*, übertragen werden. Sie übernimmt außerdem die Synchronisierung der Datenübertragung und stellt sicher, dass Pakete in der richtigen Reihenfolge gesendet und empfangen werden
2. **Link** 
	- Ist für das Packen von Daten in Frames und deren Übertragung zwischen zwei Knoten verantwortlich. Diese Schicht wird im OSI-Modell auch als Schicht 2 bezeichnet. Sie ist für die *Fehlererkennung und -korrektur zuständig* und stellt sicher, dass Datenframes während der Übertragung nicht beschädigt werden
3. **Network**
	- Die Netzwerkschicht ist für die Weiterleitung von Paketen an ihr Ziel verantwortlich. Sie *übernimmt die Adressierung* und stellt sicher, dass jedes Paket an das richtige System gesendet wird. **IP** (Internet Protocol), **ICMP** (Internet Control Message Protocol) und **ARP** (Address Resolution Protocol)
4. **Transport**
	- [[4. Semester/Rechnernetze/Transportschicht/TCP|TCP]] (Transmission Control Protocol) und [[UDP]] (User Datagram Protocol) sind zwei gängige Protokolle dieser Schicht. Diese Protokolle ermöglichen eine *zuverlässige Kommunikation* zwischen zwei Systemen und stellen sicher, dass Daten korrekt und problemlos übertragen werden.
5. **Application**
	- ist für die Bereitstellung von Diensten und Anwendungen verantwortlich, die die zugrunde liegenden Protokolle zur Kommunikation nutzen.