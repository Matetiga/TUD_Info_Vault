## Eigenschaften 
Transmission Control Protocol
- **zuverlässiges** verbindungsorientiertes Protokoll
- beliebige Nachrichtenlänge, als Pakete von max. 64 KByte übertragen
- *Reihenfolgegarantie*, 32-Bit-Folgenummern
- **Verbindungsauf-/abbau** mit [[Drei Wege Handshake]]
- Fenster-basierte Flusskontrolle und Congestion Control
- Fehlerbehandlung durch erweitertes Prüfsummenverfahren

### Struktur 
![[Pasted image 20250626123804.png]]

### Verbindungsaufbau/abbau
![[Pasted image 20250626124544.png]]

## TCP Pseudo Header 
### Checksum 
 - Werden genutzt um zu verifizieren, dass ein Paket richtig zugestellt wurde
 - Wird von einem Pseudo Header berechnet
 - Pseudo Header (vor dem TCP-Header eingefügt)
 - Der Empfänger fügt den Pseudo Header ebenfalls vor dem TCP-Paketkopf ein und berechnet die Checksumme ==analog==

---

## Vergleich mit [[UDP]]
![[Pasted image 20250701110902.png]]
- Vollduplex: Von den zwei Seiten gleichzeitige Kommunikation 