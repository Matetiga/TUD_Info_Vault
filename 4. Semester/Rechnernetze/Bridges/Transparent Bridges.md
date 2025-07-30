Devices on the Network are unaware of the Presence of this Bridge
## Wieterleitungstabelle 
- Automatischer Aufbau von Weiterleitungstebellen (**unterschiedlich** wie bei [[4. Semester/Rechnernetze/Bridges/Bridge|Bridge]])
	- Learns **MAC addresses dynamically** by observing frame traffic and builds a forwarding table.
- Tabellen initial leer 
### Funktionsweise 
Netztopologie wird durch Quelladdressen erkennt
-  Bridge empfängt an allen Ports Frames falls noch nicht bekannt,  trage Absender-Adresse und Port in SAT-Tabelle ein
- **Suche Ziel-MAC-Adresse in Weiterleitungstabelle** → Ausgabeport
- falls Suche *erfolgreich* → Sende Frame an Ausgabeport
- falls Suche *erfolglos* → Sende an alle Ausgangsports  (Fluten / Broadcast)
Einträge werden nach einer Zeit gelöscht um die Netztopologie anzupassen

![[Pasted image 20250502121850.png]]
