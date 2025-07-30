
## Gleichmässiger Kode
$$
\begin{gather}
l_{m}=\left\lceil  \frac{H_{m}}{H_{K}}  \right\rceil \quad \text{ mit  } H_{K}=1\\
\Leftrightarrow\\
\text{ falls Wahrscheinlichkeiten gleichverteilt} : l_{m}=\frac{ld(N)}{H_{K}}\\
\Leftrightarrow\\
l_{m} = \lceil ld(N) \rceil 
\end{gather}
$$

---
## Für Ungleichmässiger Kode
##### (Mit Hilfe von Shannon-Fano oder Huffman Methode)
somit erhält man die Kodelänge jedes Zeichens
### $$l_{m}=\sum^{N}_{i=1} p(x_{i})*l_{i}$$
- mit $i\in \{1,2, \dots, N\}$
- $p(x_{i})$: Wahrscheinlichkeit jedes Zeichens (Auftrittswahrscheinlichkeit)
- $l_{i}$ : Kodelänge jedes Zeichens (mit [[Huffman - Fano Verfahren]] *bestimmt*)

---
## Einheit:
$$
\frac{KZ}{QZ}
$$

---

## Kodeworterlänge ist immer grösser als Quellenentropie
### $H_{m}\leq l_{m}<H_{m}+1$
