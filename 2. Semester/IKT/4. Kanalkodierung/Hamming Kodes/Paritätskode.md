### (n, $l$, $d_{min}$) Paritätskode
- mit =>
	- $l=n-1$
	- $d_{min}=2$
	- $f_{e}=1$
---
## Beispiel
- $(3,2,2)PK$
- $A: \{ 000, 011,11,110 \}$ => jede dritte Stelle ist ein [[Paritätsbits]]
 
$$
\begin{gather}
G_{l \times n}=G_{2 \times 3}=[I_{2}C]=\begin{pmatrix}
1 & 0 & 1 \\
0 & 1 & 1
\end{pmatrix} \text{ die erste 2 Spalten sind I, die letzte C}
\end{gather}
$$
$$
H_{k \times n}=H_{1 \times 3}=[C^{T}I_{1}]=\begin{pmatrix}
1&1&1
\end{pmatrix}
$$
- falls die gesamt Summe von $s$ nicht $= 0$ ist, wird ein **Fehler erkannt**
![[WhatsApp Image 2024-07-18 at 19.05.31.jpeg]]
