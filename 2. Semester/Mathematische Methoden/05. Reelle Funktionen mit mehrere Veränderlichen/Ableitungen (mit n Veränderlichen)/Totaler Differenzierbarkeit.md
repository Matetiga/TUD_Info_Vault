## Beweis
Sei $X\to \mathbb{R}^{n}$ eine Offene Menge

### Bedingugen
=> Ist $f:X\to \mathbb{R}$ in einer Umgebung von $x_{0}\in X$ [[Partiell differenzierbar]]
und in $x_{0}$ stetig partiell differenzierbar

#### Dann:
Ist $f$ in $x_{0}$ total differenzierbar

---
## Total differenzierbar mit einer Vektor a
Sei $X\to \mathbb{R}^{n}$ eine Offene Menge

$f:X\to \mathbb{R}$ heisst in $x_{0} \in X$ **total Differenzierbar**, *wenn* es<span style="color:#ffff00"> einen Vektor</span> $a \in \mathbb{R}^{n}$ <span style="color:#ffff00">und eine Funtkion</span> $R: X\to \mathbb{R}$ gibt, so dass:
$$
\begin{gather}
f(x)=f(x_{0})+a\cdot(x-x_{0})+R(x,x_{0})\\
\\
\text{ mit }\\
\\
\lim_{ x \to x_{0}} \frac{R(x,x_{0})}{\mid\mid x-x_{0}\mid\mid}=0 
\end{gather}
$$
und **a Skalarprodukt** => *Vektor a* wird <span style="color:#ffff00">totale Ableitung</span> von $f$ in $x_{0}$ gennant

### Berechnung der Ableiung
Sei $X\to \mathbb{R}^{n}$ eine Offene Menge
Ist $f:X\to \mathbb{R}$ in $x_{0}\in X$ **total differenzierbar mit der Ableitung a**,

d.h: $f(x)\approx f(x_{0})+a\cdot(x-x_{0})$ in der Umgebung $x_{0}$
dann gilt: 
$f'(x_{0}):=a=\nabla f(x_{0}) \text{ als Gradient von f in }x_{0}$
### Es gilt:
$$
f(x_{0})+f'(x_{0})\cdot(x-x_{0})=f(x_{0})+\nabla f(x_{0})\cdot(x-x_{0})
$$


---

## Total differenzierbar mit einer Matrix A
[[Jacobi-Matrix]]
---


## Implikationen

$f$ total diff. $\implies$ $f$ partiell diff. 

$f$ stetig partiell diff. $\implies$ $f$ total diff.

---

