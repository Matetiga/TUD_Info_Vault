## Stop and Wait Protokoll 
- Der Sender schickt ein Datenpaket an den Empfänger und wartet auf eine Bestätigung (**ACK**)
- Der Sender stoppt die Übertragung weiterer Pakete, bis er ein ACK vom Empfänger erhält, das bestätigt, dass das Paket korrekt empfangen wurde


### Nachteil 
**Niedrige Effizienz**
- Da der Sender nach jedem Paket auf die Bestätigung wartet, ist die Kanalnutzung ineffizient, besonders bei hohen Latenzzeiten (z. B. in Satellitenverbindungen), da der Sender oft untätig wartet
Fenstergröße ist immer 1