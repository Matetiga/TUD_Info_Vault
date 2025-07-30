## K- dimensionaler Baum
- Organisierung in Binärbaumstruktur
- Knoten sind jeweils Trennebene
- Blätter enthalten Primitive

## Aufbau des KD-Bäumes
1. Setze äußere Hülle um alle Primitive
2. setze neue Trennebene zwischen gleich großen Gruppen an Primitiven
3. Wiederhole 2. bis alle primitive einzeln sind


Beginne mit einer Liste aller Punkten, die zu KD-Baum hinzugefügt werden
- sortiere die Punkte nach Median
- Medianpunkt muss der Wurzel des Bäumes sein
- Teile die Liste in zwei Unterlisten
	- Eine Liste enthält alle Punkte, links vom Mediam
	- Andere Liste enthält alle Punkte, rechts von Median
- Rekursiv bis alle Puntken einzeln zugeordnet würden

### Aufstellung nach Hüllvolume hierarchie
- (mit: falls die Unterteilung eine ungerade Anzahl an Objekte hat, sollte die linke Unterteilung mehr Objekte drin haben)
- *1. Unterteilung:* Rot
- *2. Unterteilung:* : Blau
- *3. Unterteilung:* : Lila

![[Screenshot from 2024-07-14 15-13-53.png]]