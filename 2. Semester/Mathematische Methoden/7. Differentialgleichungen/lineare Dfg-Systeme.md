$$
y'=A\cdot y+a
$$
ist ein lineares Dgl-System **1. Ordnung** mit *konstanten Koeffizienten*
- *Koordinaten des* <span style="color:#ffff00">Vektors a</span> sind fest vorgegebene **Funktionen**
- <span style="color:#ffff00">y ist ein Vektor</span> der gesuchten Funktionen

$$
y=
\begin{pmatrix}
y_{1}(x)\\
\dots \\
y_{n}(x) 
\end{pmatrix}
, \quad y'=
\begin{pmatrix}
y'_{1}(x)\\
\dots \\
y'_{n}(x)
\end{pmatrix}
, \quad a=
\begin{pmatrix}
a_{1}(x)\\
\dots \\
a_{n}(x)
\end{pmatrix}
, \quad A=
\begin{pmatrix}
a_{11}& \dots & a_{1n}\\
\dots \\
a_{n1}&\dots& a_{nn}
\end{pmatrix}

$$
#### Gesucht sind ALLE Funktionen $y_{1}(x),\dots,y_{n}(x)$
- so dass beim Einsetzen alle Gleichungen des Systems erfüllt sindd

---

### Diagonalisierung A
- Wenn es eine invertierbar **Matrix P existiert**, sodass $P^{-1}\cdot A\cdot P$ eine **Diagonalmatrix** ist [[Gesuchte Funktionen als Linearkombination]]
- wenn eine Basis $\mathbb{R}^n$ existiert, die aus **Eigenvektoren aus A besteht**