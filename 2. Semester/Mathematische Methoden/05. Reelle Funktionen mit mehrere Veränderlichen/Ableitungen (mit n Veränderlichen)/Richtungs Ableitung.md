Sei $X\to \mathbb{R}^{n}$ eine Offene Menge 
$f:X\to \mathbb{R}$ heisst in $x_{0} \in X$ in Richtung eines Vektors $v\in\mathbb{R}^{n}$ mit $\mid\mid v\mid\mid=1$ differenzierbar, wenn:

$$
\frac{df}{dv}(x_{0}):=\lim_{ h \to0 } \frac{f(x_{0} +hv)-f(x_{0})}{h}
$$
#### Partielle Ableitungen sind Richtungsableitungen in Richtung des i-ten Einheitsvektor $e_i$
$$
\frac{df}{dv}(x_{0}):=\lim_{ h \to0 } \frac{f(x_{0} +he_{i})-f(x_{0})}{h}
$$

---

## Berechnung Richtungsableitung
Sei $X\to \mathbb{R}^{n}$ eine Offene Menge 
$f:X\to \mathbb{R}$ in $x_{0} \in X$ differenzierbar
=> Dann existiert zu jeder Richtung $v\in\mathbb{R}^{n}$ die Richtungsableitung:
$$
\frac{df}{dv}(x_{0},y_{0})=\nabla f(x_{0},y_{0})\cdot \frac{v}{\mid\mid v\mid\mid}
$$

### Bemerkung:
$$
\frac{df}{dv}(x_{0})=\nabla f(x_{0})\cdot \frac{v}{\mid\mid v\mid\mid}=\mid\mid \nabla f(x_{0})\mid\mid\cdot 1\cdot \cos(\nabla f(x_{0}),v)
$$
$$
\nabla f(x_{0})\text{maximal}\Leftrightarrow\cos(\nabla f(x_{0}),v)=1 \Leftrightarrow \nabla f(x_{0}) \text{ parallel zu } v
$$
$$
\nabla f(x_{0})=0\Leftrightarrow\cos(\nabla f(x_{0}),v)=0 \Leftrightarrow \nabla f(x_{0}) \text{ orthogonal zu } v
$$