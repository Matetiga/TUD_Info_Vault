## Definition
Eine diskrete Zufallsgröße $X$ nimmt Werte $x_1, x_2, \dots$ mit Wahrscheinlichkeiten $p_i = p(X = x_i) > 0 \; (i = 1, 2, \dots)$ an und es gilt:

$$
\sum_{i=1}^\infty p_i = 1.
$$

$$
\begin{pmatrix}
x_1 & x_2 & \dots \\
p_1 & p_2 & \dots
\end{pmatrix}
$$

wird **Wahrscheinlichkeitsverteilung von $X$** genannt.
### Verteilungsfunktion
- [[Verteilungsfunktion]]
Die Verteilungsfunktion von $X$ ist eine Treppenfunktion :

$$
F_X(x) = p(X < x) = 
\begin{cases} 
0, & x \leq x_1 \\ 
p_1, & x_1 < x \leq x_2 \\ 
p_1 + p_2, & x_2 < x \leq x_3 \\ 
\vdots 
\end{cases}
$$
---
## Beispiel 
![[Pasted image 20250123120412.png]]