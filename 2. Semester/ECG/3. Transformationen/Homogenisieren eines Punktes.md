### 1. Schritt
- Hinzufügen eines: <span style="color:#ffff00">1</span> (**w-Komponent**)
- w-Komponente definiert Abstand zur Kamera (perspektivische Transformation) 

$$
p=
\begin{bmatrix}
p_{x} \\
p_{y}
\end{bmatrix}
\implies
\hat{p}=
\begin{bmatrix}
p_{x} \\
p_{y} \\
1
\end{bmatrix}
$$

### 2. Schritt
$$
\{M, t\}=\hat{M}
\begin{bmatrix}
M_{11}&M_{12}&t_{x} \\
M_{21}&M_{22}&t_{y} \\
0&0&1
\end{bmatrix}
$$
### 3. Schritt
$$
\hat{p}'=\hat{M}\cdot\hat{p}
$$
- $\hat{p}'$  ist homogenisiert (hat w-komponente )

##### Nicht-homogenisierung $\hat{p}'$
- wegnehmen des w-Komponentes
$$
p'= \frac{1}{w}\hat{\cdot}p'\implies p'
\begin{bmatrix}
x \\
y
\end{bmatrix}
$$

