![[Pasted image 20250515185303.png]]

---
## [[Polynomielle Reduktion|Polynomielle]] Lösung für Rucksack
- Mittels dynamische Programmierung kann man Rucksack in Zeit $O(nl)$ lösen
- Dieses Problem **zeigt nicht das** $\text{ Rucksack } \in P$ 
### Initializierung:
- Erzeuge $(l+1)\times(n+1)$ Matrix $M$
- Setze $M(g,0)=M(0,i)=0 \quad \forall 1\leq g\leq l \text{ und } 1\leq i\leq n$

### Berechnung
Für $i=0,\dots,n-1$ berechne $M(g,i+1)$ als $M(g, i + 1) := max (M(g, i), M(g − g(i + 1), i) + v(i + 1))$
- Falls: $g-g(i+1) <0$ dann verwendet man immer $M(g,i)$
- $M(g,i)$ :  *größter Gesamtwert unter den ersten i Gegenständen bei Einhaltung des Gewichtslimits g*

### Akzeptanz 
Akzeptiere falls $M$ einen Eintrag $\geq w$ hat

#### Beispiel
![[Pasted image 20250515192511.png]]

--- 

## NP-Vollständig
Nur falls die Gewichte der Gegenstände über-polynomiell wachsen dürfen
	- So ein Problem ist nur interesant, wenn das Rucksack ein großes Speicher hat 
