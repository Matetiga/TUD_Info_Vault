## Polynomielle Zeit berechenbar 
Eine totalle Funktion $f$ ist in *polynomielle Zeit berechenbar*, wenn es eine polynomiell zeitbeschränkte DTM $M$ gibt, die $f$ berechnen mit : $f_{M}=f$

---
## Logarithmischer Speicher berechenbar
Eine totale Funktion $f$ ist in *Logarithmischer Speicher berechenbar*, wenn es eine 3-Band DTM $M$, die $f$ wie folgt berechnet:
1. Die Eingabe befindet sich auf dem schreibgeschützten **Eingabeband**
2. Die DTM verwendet **maximal** $O(log n)$ Speicherzellen auf dem **Arbeitsband**
3. Die Ausgabe wird auf das Ausgabeband geschrieben (pro Zelle einmaliges Schreiben, kein Lesen)


---
## Polynomielle [[Many-One Reduktion]]

Eine **polynomiell** berechenbare totale Funktion $f : Σ^{*}→ Σ^{*}$ ist eine *polynomielle Many-One-Reduktion* von einer Sprache *P* auf eine Sprache *Q* (in Symbolen: $P ≤_{m} Q$), wenn für alle Wörter $w ∈ Σ^{*}$ gilt:
- $$w ∈ P \Leftrightarrow f (w) ∈ Q$$
### Komplexität durch Reduktion zeigen 
#### Satz
Falls $A ≤_{p} B$ und $B \in PTime$, dann ist $A \in PTime$