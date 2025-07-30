## Slow Start (Staubehandlung)
Überlastfenster wird nach Timeout auf Initialwert gesetzt, Schwellwert auf Hälfte des Überlastfensters vor Timeout reduzier
- Timeout wird verdoppelt → verlängert Zeit bis Fehlerbehandlung

## Fast Recovery (Schnelle Fehlerbehandlung)
- Wiederholung der Übertragung nach Erhalt dreier gleicher ACKs
- Sendefenster halbiert, keine Erhöhung des Timeout


![[Pasted image 20250626125241.png]]
