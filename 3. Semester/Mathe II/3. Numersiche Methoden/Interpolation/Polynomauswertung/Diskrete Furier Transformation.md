- Sei **w** eine [[primitiven n-ten Einheitswurzel|primitive (n+1)-ten Einheitswurzel]]

---
## DFT-Matrix
Polynomauswertung an den Stützstellen  $w^{0},w^{1},\dots,w^{n}$
$D_{n+1,w}:=V(w^{0}, w^{1},\dots,w^{n})=(w^{i\cdot j})_{i,j=0,1,\dots ,n}$
- mit: 
$$
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
---

## Inverse DFT
Sei $\omega$ eine primitive $(n+1)$-te Einheitswurzel im Körper $K$.

**Polynominterpolation** zu den Interpolationsbedingungen:  
- $(\omega^0, y_0), (\omega^1, y_1), \ldots, (\omega^n, y_n)$
  $(D_{n+1, \omega})^{-1} = V(\omega^0, \omega^1, \ldots, \omega^n)^{-1} = \frac{1}{n+1} \cdot V((\omega^{-1})^0, (\omega^{-1})^1, \ldots, (\omega^{-1})^n) = \frac{1}{n+1} \cdot D_{n+1, \omega^{-1}}$
  $$\frac{1}{n+1} \cdot D_{n+1, \omega^{-1}}
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
  \end{pmatrix}$$
