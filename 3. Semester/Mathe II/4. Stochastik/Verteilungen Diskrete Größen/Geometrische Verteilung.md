## Definition
Die **Geometrische Verteilung** beschreibt die Wahrscheinlichkeit, dass der erste Erfolg im **n-ten Versuch** auftritt **bei einer Bernoulli-Kette** (z. B. Würfeln oder Münzwurf), wobei jeder Versuch **unabhängig** ist

- [[Binomialverteilung#Unterschiede mit andere Verteilungen]]

- $X$ gibt die Anzahl der Bernoulli-Versuche bis zum ersten Erfolg an.
	- mit **Erfolgswahrscheinlichkeit** $p$
- $X$ hat die **Wertemenge** $\{1,2,\dots\}$ und die **Wahrscheinlichkeitsverteilung**  
  $$
  \begin{pmatrix}
  1 & 2 & \dots \\
  p_1 & p_2 & \dots
  \end{pmatrix}
  $$

  mit :
$$
  p_i = p(X = i) = (1 - p)^{i - 1} p, \quad \text{für } i = 1, 2, \dots
  $$
  und  
  $$
  \sum_{i=1}^{\infty} p_i = \sum_{i=1}^{\infty} p (1 - p)^{i - 1} = p \sum_{i=1}^{\infty} (1 - p)^{i - 1}
  $$  $$
  = p \sum_{k=0}^{\infty} (1 - p)^k = p \cdot \frac{1}{1 - (1 - p)} = 1.
  $$


---
## Erwartungswert
$$E(\mathcal{X})=\frac{1}{p}$$

### Varianz
$$
\text{Var}(\mathcal{X})=\frac{1-p}{p^{2}}
$$

---

# Gedächtnislosigkeit
- für alle $x,y$ gilt:
- folgt aus [[Bedingte Wahrscheinlichkeit]]
	$p(\mathcal{X}>x+y| \mathcal{X}>x)=p(\mathcal{X}>y)$



---

## Sammelbild problem 
![[Pasted image 20250130114517.png]]

- mit : 
	- $E(\mathcal{X_{i}})=\frac{1}{p_{1}}=\frac{n}{n-i+1}$

- Damit kann man den Erwartungswert von $X$ berechnen:
$$
  \mathbf{E(X)} = E\left(\sum_{i=1}^{n} X_i\right) = \sum_{i=1}^{n} E(X_i) = \sum_{i=1}^{n} \frac{n}{n - i + 1}
  $$
  $$
  = n \cdot \sum_{i=1}^{n} \frac{1}{n - i + 1} = n \sum_{i=1}^{n} \frac{1}{i}
  $$
- Die harmonische Zahl:
  $$
  H_n := \sum_{i=1}^{n} \frac{1}{i} \text{ heißt n-te harmonische Zahl}
  $$

- Es gilt:
$$
  H_n = \ln n + 0.57721 \dots + O\left(\frac{1}{n}\right)
  $$
  *(Euler-Konstante: $\lim_{n \to \infty} 0.57724\dots$)*
- Daraus folgt:
  $$
  \Rightarrow \quad \mathbf{E(X) \approx n \cdot \ln n}
  $$
  *(erstaunlich kurze Wartezeit! 🚀)*
