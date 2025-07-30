## w-Komponente:
- = 0 -> Vektor
- = 1 -> Punkt
Punkt + Punkt nicht möglich
Vektor + Punkt, Vektor + Vektor möglich


---
## 1. Schritt: Homogenisierung
- [[Homogene Matrix]]
- [[Homogenisieren eines Punktes]]
$$
p=
\begin{bmatrix}
x \\
y
\end{bmatrix}\implies
\hat{p}
\begin{bmatrix}
x \\
y \\
1
\end{bmatrix}
$$
## 2. Schritt: Transformation
$$
\hat{p}'=
\begin{bmatrix}
x' \\
y' \\
w'
\end{bmatrix}
$$

## 3. Schritt: w-Clip
- w-Komponente <=> Abstand zur Kamera
$$
p'=
\begin{bmatrix}
\frac{x'}{w'} \\
\frac{y'}{w'}
\end{bmatrix}
$$