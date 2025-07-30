## Definition
- $T: \mathbb{K}^{n+1} \to \mathbb{K}^{n+1}$:  
  $$\begin{pmatrix}
  a_0 \\
  a_1 \\
  \vdots \\
  a_n
  \end{pmatrix}
  \mapsto
  \begin{pmatrix}
  y_0 \\
  y_1 \\
  \vdots \\
  y_n
  \end{pmatrix}
  \quad mit    \quad
  V(x_0, x_1, \dots, x_{n})\cdot 
  \begin{pmatrix}
  a_0 \\
  a_1 \\
  \vdots \\
  a_n
  \end{pmatrix}
  =
  \begin{pmatrix}
  y_0 \\
  y_1 \\
  \vdots \\
  y_n
  \end{pmatrix}
  $$
  $V(x_0, x_1, \ldots, x_n)$ ist die **Vandermonde-Matrix** [[Vandermonde Matrix mit w]]

---

- **$T$ ist bijektiv** genau dann, wenn die inverse Matrix $V(x_0, x_1, \ldots, x_n)^{-1}$ existiert.
### Bemerkung: Determinante
  Die Matrix $V(x_0, \ldots, x_n)^{-1}$ existiert genau dann, wenn : 
$$\det(V(x_0, \ldots, x_n)) \neq 0 \quad \Leftrightarrow \quad \{x_0, x_1, \ldots, x_n\} = n + 1 \quad \text{(ist erfüllt).}$$
- Also existiert die inverse Abbildung $T^{-1}$.

---

## Beispiel 
![[IMG_2506.jpeg]]