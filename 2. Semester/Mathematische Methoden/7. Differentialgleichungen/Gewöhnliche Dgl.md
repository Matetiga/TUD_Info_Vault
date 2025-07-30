## Lineare Dgl 1. Ordnung 
- Homogene [[lineare Dfg-Systeme]] 1. Ordnung *mit Konstaten Koeffizienten* sind **immer lösbar**
$y'(x)+c\cdot y(x)=f(x)$

$$
\begin{gather}
y'=k\cdot y\\
\Leftrightarrow\\
y=C\cdot e^{kx}
\end{gather}
$$
---
#### $\not\equiv$ Symbole
- wird benutzt, wenn man ausdrücken will, dass $y(x)$ nicht die konstante Funktion ist, die überall den Wert $0$ hat

$$
y^{(n)}=f(x, y, y', \dots, y^{(n-1)})
$$hat eine allgemeine Lösung =>
$$
y = g(x, c_{1}, c_{2}, \dots, c_{n}) \text{ mit }c_{1},c_{2},\dots,c_{n} \in \mathbb{R}
$$

---

### Beispiel
- Bestimmung der Ableitung $T'(t)$ mit Hilfe der Funktion $T(t)$
$$
\begin{gather}
T'(t) = k(T(t)-20)\\
\Leftrightarrow\frac{dT}{dt}=k\cdot(T(t)-20)\\
\Leftrightarrow\frac{dT}{T(t)-20}=k\cdot dt\\
\Leftrightarrow\int \frac{dT}{T(t)-20} = \int k \, dt\\
\Leftrightarrow\ln(T(t)-20)=k\cdot t+C\\
\Leftrightarrow T(t)-20=e^{kt+C}\\ 
\Leftrightarrow T(t)=e^{kt} \cdot e^{C}+20  \text{ mit } e^{C}>0 \\
\Leftrightarrow T(t) = 20+K\cdot e^{kt}

\end{gather}
$$
- man muss dann eine Probe machen ($T(t) \text{ ableiten}$)

