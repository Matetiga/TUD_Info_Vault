## Eigenschaften 
- NP ist **nicht symmetrisch** (also es ist nicht unter Komplement abgeschossen)
	- *P* ist unter komplement abgeschlossen
	- Jedes Problem in NP ist polynomiell [[Polynomielle Verifikator|verifizierbar]]


![[Pasted image 20250512130955.png]]

## NP- Schwer
wenn jede **Sprache** in NP polynomiell darauf reduzierbar ist
### Beispiele
- Das Halteproblem ist NP-schwer, aber *sicher nicht in NP*. <span style="color:#ffff00">Gleiches gilt für jedes unentscheidbare Problem</span>
- Primzahl ist in NP, aber *vermutlich nicht NP-schwer*. <span style="color:#ffff00">Gleiches gilt für viele Probleme in P</span> (bei einigen ist dagegen sicher, dass sie nicht NP-schwer sind)

---
## NP-Vollständig 
wenn sie NP-schwer ist und in NP liegt.

### Beweis Mehtode
Um zu zeigen das ein Problem $L$ NP-vollständig ist :
- Zeige, dass $L \in NP$
- finde bereits eine bekannte NP-vollständige Problem $Q$, sodass gilt :
	- $Q \leq_{p} L$
### Beispiele
-  SAT (NP-Vollständig)
- **Clique** : (Eine Clique ist ein Graph, bei dem jeder Knoten mit jedem anderen direkt durch eine Kante verbunden ist)
- **Unabhängige Menge** :  ( es lässt sich *mit einer Clique* beweisen, da wenn es eine Clique mit $k$ Knoten, dann hat diese Clique ein **Komplementäres** Graph mit $k$ *unabhängige Knoten*)
- 

---