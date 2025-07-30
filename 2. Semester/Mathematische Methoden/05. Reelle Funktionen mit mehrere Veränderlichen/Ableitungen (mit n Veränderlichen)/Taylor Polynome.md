[[Taylor Reihe]]
## Taylor-Polynom 1. Grad <=> Lineare Nährungsfunktion

$$
\begin{matrix}
\phi'(t)&=&f_{x}(x_{0},y_{0})\cdot(x-x_{0})+f_{y}(x_{0},y_{0})\cdot(y-y_{0})\\
f_{1}(x,y)&=&f(x_{0},y_{0})+\begin{pmatrix}
x-x_{0} \\
y-y_{0}
\end{pmatrix}^{T} 
\cdot \begin{pmatrix}
f_{x}(x_{0},y_{0}) \\
f_{y}(x_{0},y_{0})
\end{pmatrix} \\
f_{1}(x,y)&=&f(x_{0},y_{0})+ f_{x}(x_{0},y_{0})\cdot(x-x_{0})+f_{y}(x_{0},y_{0})\cdot(y-y_{0})\\
\end{matrix}
$$

---

## Taylor-Polynom 2. Grad <=> Quadratische Nährungsfunktion
$$
\phi''(0)=f_{1}+\frac{1}{2}(f_{xx}(x_{0},y_{0})\cdot(x-x_{0})^{2}+2f_{xy}(x_{0},y_{0})\cdot(x-x_{0})\cdot(y-y_{0})+f_{yy}(x_{0},y_{0})\cdot(y-y_{0})^{2})

$$
$$
f_{2}(x,y)=
f(x_{0},y_{0})+\begin{pmatrix}
x-x_{0} \\
y-y_{0}
\end{pmatrix}^{T} 
\cdot \begin{pmatrix}
f_{x}(x_{0},y_{0}) \\
f_{y}(x_{0},y_{0})
\end{pmatrix}
+ \frac{1}{2}
\begin{pmatrix}
x-x_{0} \\
y-y_{0}
\end{pmatrix}^{T} 
\cdot
\begin{pmatrix}
f_{xx}(z_{0},y_{0})&f_{xy}(z_{0},y_{0}) \\
f_{yx}(z_{0},y_{0})&f_{yy}(z_{0},y_{0})
\end{pmatrix}
\cdot
\begin{pmatrix}
x-x_{0} \\
y-y_{0}
\end{pmatrix}
$$
