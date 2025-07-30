## Umkehr von [[Polynomauswertung T]]
- $T^{-1}: \mathbb{K}^{n+1} \to \mathbb{K}^{n+1}$
$$
  \begin{pmatrix}
  y_0 \\
  y_1 \\
  \vdots \\
  y_n
  \end{pmatrix}
\mapsto
\begin{pmatrix}
  a_0 \\
  a_1 \\
  \vdots \\
  a_n
  \end{pmatrix}
  \quad mit    \quad
  V(x_0, x_1, \dots, x_{n})^{-1}\cdot 
  \begin{pmatrix}
  y_0 \\
  y_1 \\
  \vdots \\
  y_n
  \end{pmatrix}
=
  \begin{pmatrix}
  a_0 \\
  a_1 \\
  \vdots \\
  a_n
  \end{pmatrix}
  $$
  - Man benötigt die Matrix $V(x_0, x_1, \dots, x_{n})^{-1}$ [[Vandermonde Matrix mit w#Inverse Vandermonde Matrix]]
  - Aufwand der Berechnung kann dekrementier werden wenn: 
	  - $x_{i}=w^{i} \quad \text{ mit } i=\{ 0,1,\dots,n \}$
	  - $w$ als eine [[primitiven n-ten Einheitswurzel|primitive (n+1)-ten Einheitswurzel]] im [[Körper]] $K$

---

![[Bemerkungen für w]]