## Eigenwert
- Ein Element $k$ eines Körpers $K$ wird **Eigenwert** einer Quadratischen Matrix $A \in \mathbb{R}^{n\times n}$gennant, wenn es ein Vektor $v \in K^{n}\backslash \{0\}$ mit:
$$
\text{ Es existiert } A\cdot v=k\cdot v 
$$
dann folgt (*eine homogenes LGS mit einer Lösung*):
$$
0_{K^{n}}=(A-k\cdot E_{n})\cdot v
$$
- $0_{K^{n}}$ : Nullvektor
- $E_{n}$ : Einheitsmatrix

---

## Bemerkung (mit Determinante)
$$
\begin{gather}
A\cdot v=k\cdot v \Leftrightarrow \det(A-k\cdot E_{n})=0
\end{gather}
$$


---

### Beispiel
$$
A=
\begin{pmatrix}
1&3 \\
0&4
\end{pmatrix}
$$
$$
\begin{gather}
\det \begin{pmatrix}
1-k&3 \\
0&4-k
\end{pmatrix}
=0\\
\Leftrightarrow\\
(1-k)(4-k)-3\cdot 0=0\\
\text{ somit sind die Eigenwerte: } k_{1}=1, \quad k_{2}=4
\end{gather}
$$


---

