## Definition
Eine **Many-One-Reduktion** ist eine Methode, um zu zeigen, dass ein Problem Q *mindestens so schwer ist wie ein Problem* P, indem man zeigt, dass P durch eine deterministische Transformation in Q umgewandelt werden kann
- Mit $P \leq_{p}Q$

Eine berechenbare **totale Funktion** $f : Σ^{*}→ Σ^{*}$ ist eine Many-One-Reduktion von einer
Sprache *P* auf eine Sprache *Q* (in Symbolen: $P ≤_{m} Q$), wenn für alle Wörter $w ∈ Σ^{*}$ gilt:
$$w ∈ P \Leftrightarrow f (w) ∈ Q$$
-  Dies bedeutet, dass die **Reduktion von w muss in Q sein** 


--- 
## Vergleich mit Turing Reduktionen 
- **Jede Many-One-Reduktion** kann als [[Turing Reduktionen]] ausgedrückt werden
- Es gibt Probleme P und Q, für die $P ≤_{T} Q$gilt, aber nicht $P ≤_{m} Q$
- Many-One is weniger Mächtig als Turing-Reduktion
- Turing-Reduktion versucht mit Hilfe eines [[Turing Reduktionen#Definition|Orakel]] vom Problem Q, Problem P zu lösen, während Many-One versucht ein eimailige Abbildung zu haben

---
## Semi-Entscheidbarkeit
### Satz
Wenn $P ≤_{m} Q$ und $Q$ *semi-entscheidbar* ist, dann ist **auch** $P$ *semi-entscheidbar*

---

![[Effizient berechenbare Funktionen#Komplexität durch Reduktion zeigen]]

---

