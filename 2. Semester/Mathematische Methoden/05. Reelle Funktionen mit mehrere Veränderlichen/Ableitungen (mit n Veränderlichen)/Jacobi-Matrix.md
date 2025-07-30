Sei $X\to \mathbb{R}^{n}$ eine Offene Menge

$f:X\to \mathbb{R}$ heisst in $x_{0} \in X$ total differenzierbar, wenn es eine Matrix $A\in \mathbb{R}^{m \times n}$
und eine Funktion $R:X\to \mathbb{R}^{m}$ gibt, so dass:
$$
f(x)=f(x_{0})+A\cdot(x-x_{0})+R(x,x_{0}) \text{ mit } \lim_{ x \to x_{0} } \frac{R(x,x_{0})}{\mid\mid x-x_{0}\mid\mid}=0 
$$
###### Matrix wird Totale ableitung von f genannt

### Berechnung der Ableitung
Sei $X\to \mathbb{R}^{n}$ eine Offene Menge
Ist $f:X\to \mathbb{R}$ in $x_{0}\in X$ **total differenzierbar mit der Ableitung A**,

d.h => $f(x)\approx f(x_{0})+A\cdot(x-x_{0})$ in der Umgebung $x_{0}$

#### Dann gilt:
## Jacobi-Matrix:
$$f'(x_{0}):=A=
\begin{bmatrix}
\nabla f_{1}(x_{0})^{T} \\
\dots \\
\nabla f_{m}(x_{0})^{T} 
\end{bmatrix}
=
\begin{bmatrix}
\frac{f_{1}}{dx_{1}}(x_{0})&\dots& \frac{df_{1}}{dx_{n}}(x_{0}) \\
\dots \\
\frac{df_{m}}{dx_{1}}&\dots& \frac{df_{m}}{dx_{n}}(x_{0})
\end{bmatrix}
\in \mathbb{R}^{m \times n}
$$
