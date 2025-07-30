Sei $X\subseteq \mathbb{R}^{n}$ eine Offene Menge

$f:X\to \mathbb{R}^{m}$ und  $g:X\to \mathbb{R}^{m}$  in $x_{0}\in X$ differenzierbar
=>**Dann** sind auch $f+g$ und $k\cdot f\ \ \  (k\in \mathbb{R})$in $x_{0}$ differenzierbar

### Es gilt:
- Die J[[Jacobi-Matrix]] von $j$ und $g$ werden addiert/skalarmultipliziert
$$
\begin{gather}

(f+g)'(x_{0})=f'(x_{0})+g'(x_{0}) \Leftrightarrow J_{g+f}(x_{0})=J_{f}(x_{0})+J_{g}(x_{0})\\
(k\cdot f)'(x_{0})=k\cdot f'(x_{0})\Leftrightarrow J_{kf}(x_{0})=k\cdot J_{f}(x_{0})
\end{gather}
$$


---

## Kettenregel
Sei $X\subseteq \mathbb{R}^{n}$ eine Offene Menge
$f:X\to \mathbb{R}^{m}$ sei in $x_{0}\in X$ differenzierbar und $g:f(X)\to \mathbb{R}^{p}$ sei in $f(x_{0})\in f(x)$ differenzierbar

### Dann ist: $g \circ f$ differenzierbar
$$
(g \circ f)'(x_{0})=g'(f(x_{0}))\cdot f(x_{0}) \text{ bzw.  }J_{g \circ f}(x_{0})=J_{g}(f(x_{0}))\cdot J_{f}(x_{0})
$$

#### Folgerung:
Für differenzierbare Funktionen $f,g$ mit 
$$f:\mathbb{R}\to \mathbb{R}^{n}:t \mapsto
\begin{pmatrix}
f_{1}(t) \\
\dots \\
f_{n}(t)
\end{pmatrix},
g:\mathbb{R}^{n}\to \mathbb{R}:
\begin{pmatrix}
x_{1} \\
\dots \\
x_{n}
\end{pmatrix}
\mapsto g
\begin{pmatrix}
x_{1} \\
\dots \\
x_{n}
\end{pmatrix}
\text{ gilt: }
$$
$$
(g \circ f)'(t)= \frac{dg}{dx_{1}}(f(t))\cdot f_{1}'(t)+\dots+ \frac{dg}{dx_{n}}(f(t))\cdot f'_{n}(t)
$$

