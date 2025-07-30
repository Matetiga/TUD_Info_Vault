### Wenn die Matrix $A$ diagonalisierbar ist 

---
## 1. Bestimmung der Eigenwerte von $A$
- [[Berechnung Eigenwerte]]
- [[Bestimmung Determinante]]


## 2. Bestimmung einer Basis zu jedem Eigenraum
- Eigenvektoren sind eine Basis eines Eigenräumes [[Berechnung Eigenvektoren]]
- [[Bestimmung des Kerns einer Matrix]]
### Falls die gefundene Eigenvektoren von $A$ eine Basis von $K^{n}$ sind, dann **A diagonalisierbar**


##  3. Diagonalisierung
- falls die Summe der Dimensionen der Eigenräume gleich $n$ sind, dann ist $A$ **diagonalisierbar**
- Die Matrix $P$ hat als Spalten die Vektoren einer Basis, die aus Eigenvektoren von $A$ besteht


## 4. Substitution
$$
y=P\cdot u \quad \quad \text{ Daraus folgt }  y'=P\cdot u'
$$
$$
\text{ Einsetzen in }y'=A\cdot y
$$
## 5. Lösen des Dgl-System
- Rücksubstitution lifert das Ergebnis
$$
u'=(P^{-1}A\cdot P)\cdot u
$$
- dann löst man das Dgl-System mit $y'=k\cdot y \implies y=C\cdot e^{kx}$
