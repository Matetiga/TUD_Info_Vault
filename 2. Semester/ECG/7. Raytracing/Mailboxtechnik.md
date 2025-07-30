- Jede Strahl erhält ein ID
- jedes Objekt erhält eine Mailbox in der die letzten Schnittberechnungen gespeichert sind (ID, Schnittinfo)
- **Vor Schnittberechnung wird Mailbox geprüft ob <span style="color:#ffffff">Schnittberechnung bereits vorhanden</span>**
- *Falls Neuberechnung:*
	- Mailbox aktualisieren

---
### Beim Raytracing
- **Anzahl der Schnittpunktsberechnungen reduzieren**
	- Genutzt für:
		- Szenen mit vielen Objekten
		- Komplexe Geometrien
		- Wiederholte Strahlenverfolgung

- Sinvoll, wenn Objekte in mehrere Bereiche der Beschleunigungsstruktur vorkommen
- man spart mehrfache Schnittberechnungen, wenn Informationen bereits in der Mailbox liegen

---
## Berechnungstechnik
- Gitter
- KD-Baum


*Hüllenvolumentechnik ist kein Mailbox Technik*
