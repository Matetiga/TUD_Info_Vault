### $$H(X,Y)=H(X)+H(Y|X)$$$$H(X,Y)=H(Y)+H(X|Y)$$
---
## Formeln:
$$
\begin{gather}
H(X,Y)=\sum^{N}_{i=1}\sum^{M}_{j=1}p(x_{i},y_{j})\ ld\left(  \frac{1}{p(x_{i},y_{j})} \right)\\
\end{gather}
$$
$$
\begin{gather}
H(X,Y)=-\sum^{N}_{i=1}\sum^{M}_{j=1}p(x_{i})p(y_{j}|x_{i})\ ld(p(x_{i})ld(p(y_{j}|x_{i})))\\
\Leftrightarrow\\
H(X,Y)=\sum^{N}_{i}p(x_{i})ld \ \frac{1}{p(x_{i})}+\sum^{N}_{i}\sum^{M}_{j}p(x_{i})p(y_{j}|x_{i}) \ ld\frac{1}{p(y_{j}|x_{i})}\\
\end{gather}
$$

mit =>
[[Markow -  Entropie]]
$$
H(Y|X)=-\sum_{i}\sum_{j}p(x_{i})p(y_{j}|x_{i}) \ ld(p(y_{j}|x_{i}))\\
$$
---

## Grenzfälle
- Vollständige Abhängigkeit :
	- Die Menge Y (X grösser als Y) liegt komplett in X
	- Dann gilt:
	- $H(X,Y)=H(X)\text{ mit Y}\in \text{X}$


- Vollständige Unabhängikeit:
	- Beide Mengen haben keine Gemeinsamkeiten
	- Dann gilt:
	- $H(X,Y)=H(X)+H(Y)$
