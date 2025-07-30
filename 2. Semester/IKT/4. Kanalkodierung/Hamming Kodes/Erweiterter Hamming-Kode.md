#### Hinzufügung eines Kontrollelementes $k_{0}$
- zusätzliches [[Paritätsbits]]
- <span style="color:#ffff00">Kann auch Doppelbitfehler erkennen</span> 
	- $f_{e}=2$
- <span style="color:#ffff00">Kann Einzelbitfehler korregieren</span> 
	- $f_{k}=1$
- $d_{min}=4$

## Bemerkung
- Die andere Kontrollstellen bleiben gleich
$$
k_{0}=\sum^{n}_{i=1}n_{i}\text{ mod }2
$$
Die andere [[Kontrollgleichungen]] bleiben gleich
$$
s_{0}=\sum^{n}_{i=0}n_{i}\text{ mod }2
$$

---
### Beispiel
- $(7,3,4)HK \to (8,4,4)HK$
- somit folgt : $H_{4 \times 8}$
$$
\begin{gather}
\begin{pmatrix}
l_{4}&l_{3}&l_{2}&k_{3}&l_{1}&k_{2}&k_{1}&k_{0}\\
1&1&1&1&0&0&0&0 \\
1&1&0&0&1&1&0&0 \\
1&0&1&0&1&0&1&0 \\
1&1&1&1&1&1&1&1 \\
n_{7}&n_{6}&n_{5}&n_{4}&n_{3}&n_{2}&n_{1}&n_{0}
\end{pmatrix}
\end{gather}
$$