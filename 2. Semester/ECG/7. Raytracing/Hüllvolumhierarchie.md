- Effiziente Datenstruktur, um Raytracing zu beschleunigen
- [[KD-Baum]]
#### Die Szene wird in Hüllvolumen hierarchisch unterteilt
- Reduziert die Anzahl der Schnittpunktsberechungen pro Strahl, indem sie schnell entscheiden, welche teile der Szene getestet werden müssen

### Schritte
- Szene wird in Hüllvolume unterteilt (*rekursiv in eine Baumstruktur repräsentiert*)
- Strahl wird von der Kamera geschikt
	- Das Strahl wird zuerst **gegen das oberste Hüllvolume getestet**
		- wenn *keine Schnittpunkte* gibt, können alle darin enthaltenen **Objekte und Subvolumen ignoriert werden**
		- wenn ein *Schnttpunkt gibt*: wird das **Strahl gegen die Kindknoten** des aktuellen Hüllvolumens getestet (bis das tatsächlich Objekt erreicht wird)

<span style="color:#ffa033">Hüllvolumen wären die Rechtecke, die die Kreise einschließen</span>
![[Screenshot from 2024-07-14 14-45-51.png]]

## Konvexe Hülle
- Innenwinkel $< 180$°
- <span style="color:#ffa033">Rechenintensiver</span>
- Bessere **Anpassung zu der Form** der eingeschlossene  Obkjekten in der Szene
	- **Minimieren das Leervolumen**

