# mit $x_{0}=0$ 

### Absolut konvergent
Bestimmung der Konvergenz mit [[Quotienkriterium]][[Wurzelkriterium]]
$$
\begin{gather}
\text{mit QK: } \lim_{ k \to \infty } |\frac{a_{k+1}x^{k+1}}{a_{k}x^{k}}|= |x|*\lim_{ k \to \infty } |\frac{a_{k+1}}{a_{k}}|<1
\end{gather}
$$---
#### 1. Fall 
$$
\lim_{ k \to \infty } |\frac{a_{k+1}}{a_{k}}|=a \in \mathbb{R}_{+} \backslash \{0\}\implies |x|*\lim_{ k \to \infty } |\frac{a_{k+1}}{a_{k}}|<1 \text{ mit } |x|< \frac{1}{a}
$$
##### $\text{ also: }r=\frac{1}{a}$

---
#### 2. Fall
$$
\lim_{ k \to \infty } |\frac{a_{k+1}}{a_{k}}|=0\implies|x|*\lim_{ k \to \infty } |\frac{a_{k+1}}{a_{k}}|<1 \text{ gilt für alle } x \in \mathbb{R}
$$
##### also $r=\infty$

---
#### 3. Fall
$$
\lim_{ k \to \infty } |\frac{a_{k+1}}{a_{k}}|=\infty\implies|x|*\lim_{ k \to \infty } |\frac{a_{k+1}}{a_{k}}|<1 \text{ gilt für } |x|=0
$$
##### also: $r=0$

---

### Dann liegt x in 