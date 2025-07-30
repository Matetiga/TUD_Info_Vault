Es gilt: $\delta= \epsilon= p_{s}$ mit $(p_{s}$  [[Schrittfehlerwahrscheinlichkeit]])


#### $H_{T}$
$$
H_{T}=H(Y)-\left( (1-p_{s})\cdot ld\frac{1}{1-p_{s}}+p_{s}\cdot \frac{1}{ld(p_{s})} \right)
$$

## $H_{T_{max}}$ 
- mit gleich verteilte Wahrscheinlichkiten 
- $p(x_{1})=p(x_{0})=\frac{1}{2}$
$$H_{T_{max}}=\left( (1-p_{s})\cdot ld\frac{1}{1-p_{s}}+p_{s}\cdot \frac{1}{ld(p_{s})} \right)$$


---
$$
\begin{gather}
p(x_{0})\gg \left| p_{s}\cdot (p(x_{1})-p(x_{0}))\right|\\
p(x_{1})\gg \left| p_{s}\cdot (p(x_{1})-p(x_{0}))\right|
\end{gather}
$$
$\gg$ "stark grösser als"

##### somit folgt:
$H(Y)\approx H(X) \text{ und } H_{T}\approx H(X)+(1-p_{s})ld(1-p_{s})+p_{s}ld(p_{s})$

