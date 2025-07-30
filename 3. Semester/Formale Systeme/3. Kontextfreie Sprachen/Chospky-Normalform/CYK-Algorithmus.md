Der CYK-Algorithmus arbeitet mit einer kontextfreien Grammatik G in [[Chomsky-Normalform CNF]]

Falls $|w| = 1$ dann ist $w ∈ Σ$ und es gilt:
- $w ∈ L(G)$ genau dann, wenn es eine Regel $S → w$ in G gibt

Falls $|w| > 1$, dann ist:
- $w ∈ L(G)$ genau dann, wenn es eine Regel $S → AB$ und einen Index $i ∈ {1, . . . , n − 1}$ gibt, so dass gilt

$A\implies^{*} \ a_{1}\dots a_{i}$ und $B\implies^{*} \ a_{i+1}\dots a_{n}$


---

## Beispiel: 
mit dem Wort : $a+b*c$
**In der Diagonal:**
- dann guckt man, *mit welchen Variable jedes Terminalsymbol erzeugen kann*

**Zweiten Diagonal:** 
- zweite Zeile, dritte Spalte **Beispiel**: *PS* kann mit *A* erzeugt werden 

**Fünfte Spalte: 
- man hat dann verschiedene Möglichkeiten um den Kästen zu erfüllen
- man probiert mit jeder Möglichkeit
	- *fünfte Spalte, erste Zeile* : **SM aus S**
	- [[#Wichtig beim vergleichen]]
#### Ziel des Algoritgmus
- zu entscheiden, ob $S \in v [1,n]$
- da 5. Spalte und 1. Zeile $\implies$ 
	- $S \in V[1,5]\to w \text{ kann erzeugt werden}$
![[Screenshot from 2024-12-02 12-23-37.png]]

### Wichtig beim vergleichen
- Man vergleicht die Kästchen, die dieselbe Farbe haben.
- Beim Beispiel: **D** wird aus **S** (*5. Spalte, 1. Zeile*) und **E** (*7. Spalte, 6 Zeile*)

![[Screenshot from 2024-12-05 14-12-05.png]]