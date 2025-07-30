# Bei Hamming kodes -> $d_{min}=3$

#### Die Anzahl der Zeichen, in denen sich zwei Kodewörter unterscheiden
$$
\begin{gather}
a_{i}=(u_{i1}, u_{i2},\dots, u_{in})\\
a_{j}=(u_{j1}, u_{j2},\dots, u_{jn})\\
\text{ Hamming Distanz }\implies d_{ij}=d(a_{i}, a_{j})=|\{g \in \{1,2,\dots,n\}|u_{ig}\neq u_{jg}\}|
\end{gather}
$$

---
## Hamming Distanz
- man bestimmt die Anzahl der unterschiedliche Zeichnen im Vergleich mit der Nullwort
$$
d(a_{i},a_{j})=\sum^{n}_{g=1}(u_{ig} \oplus u_{jg} )
$$



## Mindestdistanz
-> $d_{min}=min\ \ \  d(a_{i},a_{j})=min \ \ d(0,a_{i})=min \ \ w(a_{i})=w_{min}$
- mit $a_{i}\neq a_{j} \text{ und } a_{i}\in A \backslash \{0\}$
- FE: $f_{e}$ => Fehler Korruktur durch Wiederholung
- FK: $f_{k}$ => Fehler Korrektur durch Rekonstruktion

$$
d_{min}=f_{e}+f_{k}+1
$$
$$
\begin{gather}
f_{e}= \left\lfloor  \frac{d_{min}}{2}  \right\rfloor &f_{k}=l \left\lfloor \frac{d_{min}-1}{2}   \right\rfloor 
\end{gather}
$$

---
## [[Dichtgepäckt Kode]]