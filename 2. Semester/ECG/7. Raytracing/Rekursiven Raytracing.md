## Primärstrahlen
- Für jedes Pixel, wird ein Strahl von der Kamera durch das Pixel in die Szene geschickt 
- Primärstrahl wird verfolgt bis er ein Objekt in der Szene trifft
	- Bestimmung der Fabe des Pixels
	- Von dieser Stelle werden Strahlen richtung der Lichtquellen geschickt *(um zu prüfen ob beleuchtet oder im Schatten liegt*) -> Schattenfüller


#### Schattenfüller
- **pro Lichtquelle und Punkt einen Schattenfüller**
- prüft ob zwischen Lichtquelle und aktuellen Punk ein Objekt liegt


## Sekundäre Strahlen
- wenn Primärstrahl eine reflektierende Oberfläche trifft.
	- Diese Strahl verfolgt dann dieselbe Schitte wie für das Primärstrahl

---
### Beschränkung der Rekursionstiefe
- wenn die Szene viele Spiegelungen und Refraktionen hat
	- Berechnungsdauer geht unendlich 
	- viele Sekundärstrahlen


##### Bei Rekursionstiefe = 0 -> Dann keine Reflektion
