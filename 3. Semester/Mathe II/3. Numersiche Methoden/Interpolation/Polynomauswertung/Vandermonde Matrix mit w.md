- und **w** eine [[primitiven n-ten Einheitswurzel|primitive (n+1)-ten Einheitswurzel]]
## Definition 
$$
V(\omega^0, \omega^1, \ldots, \omega^n) =
\begin{pmatrix}
1 & \omega^0 & (\omega^0)^2 & \cdots & (\omega^0)^n \\
1 & \omega^1 & (\omega^1)^2 & \cdots & (\omega^1)^n \\
1 & \omega^2 & (\omega^2)^2 & \cdots & (\omega^2)^n \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
1 & \omega^n & (\omega^n)^2 & \cdots & (\omega^n)^n
\end{pmatrix}

$$
- [[Vandermonde-Determinante]]
### Dann gilt: 
- $V(w^{0}, w^{1},\dots,w^{n})=(w^{i\cdot j})_{i,j=0,1,\dots,n}$
- $\det V(w^{0},w^{1},\dots,w^{n})\neq 0$

---

## Inverse Vandermonde Matrix
da $\det V(w^{0},w^{1},\dots,w^{n})\neq 0 \Leftrightarrow \text{ existiert } V(w^{0}, w^{1},\dots,w^{n})^{-1}$

- somit gilt:
$D_{n+1,w}^{-1}=V(w^{0}, w^{1},\dots,w^{n})^{-1}=({n+1})^{-1}\cdot V((w^{-1})^{0}, (w^{-1})^{1},\dots,(w^{-1})^{n})=({n+1})^{-1} D_{n+1,w^{-1}}$
	- man muss dann das *Invers* zu $(n+1)^{-1}$ in $K$ bestimmen 
	- [[Diskrete Furier Transformation#Inverse DFT]]
	- [[primitiven n-ten Einheitswurzel#Beispiel]]

### Aufstellung der Inversen Matrix
- mit $w^{-1} \equiv w^{n} (\mod n+1)$
wenn man die normale (nicht invertierten Matrix) aufstellt, dann ist $D_{n+1,w}^{-1}$ die **horizontale Spiegelung** der normalen Matrix