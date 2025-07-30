Ein Kode zur Fehlererkennung und Fehlerkorrektur 
- ein **bit** wird mit einem **Wiederholungsfaktor wiederholt**
- dann wird nach Mehrheit des bits im Wort entschieden 
	- falls Mehrheit *1 bits* sind dann => **1**  
	- falls Mehrheit *0 bits* sind dann => **0**  

### Beispiel
- mit Lange = 6
1 -> 111111       aber durch Übertragungsfehler kann auch folgendes passieren
1 -> **111001**     (Dann wird nach Mehrheitsregel entschieden) -> **111111**


