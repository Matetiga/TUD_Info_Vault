Anzahl von unabhängige [[Bernoulli Verteilung|Bernoulli Verteilung]] bis zum $n$-ten Erfolg 

- Wertemenge: $\{ n,n+1,\dots \}$
- *Wahrscheinlichskeitsverteuilung*:
	- $$
	\begin{pmatrix}
n & n+1 & \dots\\
p_{n} & p_{n+1} & \dots
\end{pmatrix} 
$$

mit : $$p_{i}=p(\mathcal{X}=i)= \binom{i-1}{n-1}(1-p)^{i-n}p^{n}$$
und:  $\sum_{i=n}p_{i}=1$


#### Negative Binomialkoeffizient
- mit $\alpha \in \mathbb{R}$
$$\binom{\alpha}{i}=\frac{\alpha (\alpha-1)* \dots * \alpha(\alpha-i+1)}{i!}$$
---

### Erwartungswert
$E(\mathcal{X})=n \cdot \frac{1}{p}$


### Varianz
$\text{Var}(\mathcal{X})=n \cdot \frac{1-p}{p^{2}}$
