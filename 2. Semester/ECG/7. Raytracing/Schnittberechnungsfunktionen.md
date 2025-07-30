## Implementierung von zwei Schnittberechnungsfuktionen
- **erste Berechnungsfunktion** berechnet für jeden Schattenfühler ein Schnittobjekt
	- diese Funtkion muss sehr effizient sein, da es für die Ermittlung der Sichbarkeit von Objekte dient
	
- **zweite Berechnungsfunktion** erhaltet präzise Information über den Schnittpunkt (Position, Materialeigenschafte, Textur)


---

### Erster Schnittpunkt 
- Aufwändiger Berechnung, da sie erfordert, dass jedes Strahl **gegen alle möglichen Objekte in der Szene** für **Schnittpunkte** getestet wird

### Schattenstrahl 
- diese Berechnugn kann Unterbrochen werden, fall das Strahl ein Hinderniss trifft (liegt im Schatten)
