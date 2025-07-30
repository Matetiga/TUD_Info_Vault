mit $G=\frac{1}{R}$
## Algorithmus 
(tgiFormel:: siehe Note)
- Definiere Knotenspannvektor  (zwischen Knoten und Bezugsknoten)
- Defieniere Vektor der Strömungen
- Aufstellen der Knoten-Leitwertmatrix
	- **Hauptdiagonaleelemente**: positiveSumme aller an diesen Knoten angeschlossenen Leitwerte
	- **Nebendiagonalelemente**: negativer Leitwert zwischen dem aktuellen Knoten (Zeile) und dem Nachbarnknoten (Spalte) -> Koppelleitwert
	- Zeilensumme entspricht Leitwert zum Bexugsknoten
	- <span style="color:#ffff00">Matrix ist symmetrisch in zur Hauptdiagonale</span>

![[IMG_2439.jpeg]]
![[IMG_2440.jpeg]]
