<span style="color:#ffff00">Berechnung der Anzahl redundanter Stellen </span>$k$ bei bekannten $d_{min}$ *in Abhängigkeit* von $l$ oder $n$

## Definition:
Hamming Schranke gibt die **maximale Anzahl von Codewörtern**, die ein fehlerkorrigierenden Code mit gegebenen **Mindestabstand** $d_{min}$ und Länge  $n$


---

#### Berechnung der reduntanten Stellen $k$
- Gegeben $d_{min,}, l \text{ oder }n$
- $n=l+k$
- man pobiert mit *möglichst klein* verschiedene Werte

$$
2^{n}=2^{l} \ 2^{k}\geq 2^{l}(1+ \binom{n}{1}+\binom{n}{2}+\dots+\binom{n}{f_{k}})
$$
$$
2^{k}\geq \sum^{f_{k}}_{i=0} \binom{n}{i} 
$$
$$
k\geq ld\sum^{f_{k}}_{i=0} \binom{n}{i} 
$$
- Falls: 
$$
k=ld\sum^{f_{k}}_{i=0} \binom{l+k}{i}
$$
##### dann heißt die Kode **perfekt** oder **Dichtgepäckt**
---
- mit $f_{k}$ :
  $$
\begin{gather}
f_{e}= \left\lfloor  \frac{d_{min}}{2}  \right\rfloor &f_{k}=l \left\lfloor \frac{d_{min}-1}{2}   \right\rfloor 
\end{gather}
$$
- [[FK]]