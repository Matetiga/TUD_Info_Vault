- [[Maschensatz]]

$m=z-(k-1)$
- $k$ Knoten
- $z$ Zweigen
- $m$ unabhängige Maschengleichung

## Algorithmus
(tgiFormel:: siehe Note)
- Definiere Richtung für jede Masche (z.B.: Uhrzeigerrichtung)
- Definiere Spannungsquellerichtung (*neg. Vorzeichen, wenn Richtungssinn = Umlaufsinn der Masche*)
- Aufstellen Maschen-Impedanzmatrix
	- **Hauptdiagonalelemente**: positive Summe aller zur Masche gehörenden Wiederstände
	- **Nebendiagonalelemente**:  Summe der Wiederstände der Matrix, die vom Maschenstrom der Spalte durchflossen werden
	- <span style="color:#ffff00">Matrix ist symmetrisch zur Hauptdiagonale</span>

Vorzeichen hängt von der Richtung der (beliebig gestellte) Richtung der Masche
![[IMG_2437.jpeg]]

![[IMG_2438.jpeg]]