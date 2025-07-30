## Definition
Sei $X$ eine diskrete Zufallsgröße mit der Wahrscheinlichkeitsverteilung

$$
\begin{pmatrix}
x_1 & x_2 & \dots \\
p_1 & p_2 & \dots
\end{pmatrix}
$$

$$
E(X) := \sum_{i=1}^\infty x_i \cdot p_i
$$

heißt **Erwartungswert von $X$**, falls die **Reihe absolut konvergent** ist.  
Ansonsten existiert kein Erwartungswert für $X$.
- [[Konvergente Reihen]]

$$
\sum_{i=1}^\infty x_i \cdot p_i
$$
---

### Bermerkungen
- $E(X)$ *(Bezeichnung auch $E\mathcal{X}$)* ist ein gewichteter Mittelwert mit den Wahrscheinlichkeiten $p_i$ als Gewicht.
- Bei stetigen Zufallsgrößen verwendet man Integrale statt Summen.

---

## Beispiel
Würfeln:  
$$
E(X) = 1 \cdot \frac{1}{6} + 2 \cdot \frac{1}{6} + 3 \cdot \frac{1}{6} + 4 \cdot \frac{1}{6} + 5 \cdot \frac{1}{6} + 6 \cdot \frac{1}{6} = 3.5
$$
mit: 
- $\sum^{\infty}_{j=1}p(\mathcal{X}\geq j)=(p_{1}+p_{2}+p_{3}+\dots)+(p_{2}+p_{3}+\dots)+(p_{3}+\dots)+\dots$
![[Pasted image 20250123123435.png]]