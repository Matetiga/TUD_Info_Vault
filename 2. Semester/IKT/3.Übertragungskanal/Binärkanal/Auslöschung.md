mit  =>

$$
p(y_{j}|x_{i})=
\begin{pmatrix}
1-\epsilon-\lambda & \epsilon & \lambda\\
\delta & 1-\delta-\lambda &\lambda
\end{pmatrix}
$$

#### Die Übergangswahrscheinlichkeiten:
- $1-\epsilon-\lambda$
- $1-\delta-\lambda$
geben an, mit welcher <span style="color:#ffff00">Wahrscheinlichkeit</span>, die gesendete <span style="color:#ffff00">Binärelemente richtig empfangen werden</span> 

---

### $H_{T_{max}}$
- mit gleich verteilte Wahrscheinlichkeiten 
$$
H_{T_{max}}=(1-\lambda)-p_{s}\cdot ld\left( \frac{1}{p_{s}} \right)+(1-\lambda)\cdot ld\left( \frac{1}{(1-\lambda)} \right)-(1-p_{s}-\lambda)\cdot ld\left( \frac{1}{(1-p_{s}-\lambda)} \right)
$$
