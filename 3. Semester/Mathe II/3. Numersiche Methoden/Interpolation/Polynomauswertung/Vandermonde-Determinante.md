## Allgemein 
$$
\det V(x_{0},x_{1},\dots,x_{n}) = \prod_{i>j}(x_{i}- x_{j}) \quad mit \ i,j \in \{ 0,\dots,n \}
$$
- also Determinante $\neq0$ $\Leftrightarrow x_{0},x_{1},\dots,x_{n}$ **paarweise unterschiedlich sind**

### Bemerkung
- [[Vandermonde Matrix mit w#Inverse Vandermonde Matrix]]
  Die Matrix $V(x_0, \ldots, x_n)^{-1}$ existiert genau dann, wenn : 
$$\det(V(x_0, \ldots, x_n)) \neq 0 \quad \Leftrightarrow \quad \{x_0, x_1, \ldots, x_n\} = n + 1 \quad \text{(ist erfüllt).}$$
- Also existiert die inverse Abbildung $T^{-1}$.

---

### Berechnung der Determinante der Vandermonde-Matrix $V(x_0, x_1, \ldots, x_n)$

- Für $n = 1$:  
  $$
  \det
  \begin{pmatrix}
  1 & x_0 \\
  1 & x_1
  \end{pmatrix}
  = x_1 - x_0$$

- Für $n = 2$:    
  $$\det
  \begin{pmatrix}
  1 & x_0 & x_0^2 \\
  1 & x_1 & x_1^2 \\
  1 & x_2 & x_2^2
  \end{pmatrix}
  = \det
  \begin{pmatrix}
  1 & 0 & 0 \\
  1 & x_1 - x_0 & x_1(x_1 - x_0) \\
  1 & x_2 - x_0 & x_2(x_2 - x_0)
  \end{pmatrix}$$


  Entwicklung nach der ersten Zeile:  
  $$= \det
  \begin{pmatrix}
  x_1 - x_0 & x_1(x_1 - x_0) \\
  x_2 - x_0 & x_2(x_2 - x_0)
  \end{pmatrix}$$
  $$= (x_1 - x_0)(x_2 - x_0) \cdot \det
  \begin{pmatrix}
  1 & x_1 \\
  1 & x_2
  \end{pmatrix}$$
  
  $$= (x_1 - x_0)(x_2 - x_0)(x_2 - x_1)$$
  $$= (x_2 - x_0)(x_2 - x_1)(x_1 - x_0)$$
