## Definition 
Wird verwendet, wenn ein $\textbf{\textcolor{yellow}{Ziehen mit Zurücklegen}}$ oder eine **unabhängige Wiederholung eines Experiments** vorliegt.

---
### Unterschiede mit andere Verteilungen 
-  mit [[Hypergeometrische Verteilung]]: 
	- Hypergeometrsische Verteilung ist **ohne Zuücklegen**
- mit [[Geometrische Verteilung]]
	- Geometrsche Verteilung hat **keine feste Anzahl** an Versuche 
	- "Es wird einem idealen *Würfel 50-mal* gewürfelt. Die Zufallsgröße 𝑋 gibt die Anzahl Würfe an, in denen eine 6 geworfen wurde"

---

## Formale Def
 $X = X_1 + X_2 + \dots + X_n$ ist die Summe von $n$ unabhängigen [[Bernoulli Verteilung|Bernoulli-verteilten]] Zufallsgrößen $X_i$ $(i = 1,2,\dots,n)$ mit dem Parameter $p$;  
  d.h. es werden $n$ **unabhängige** Bernoulli-Versuche mit Parameter $p$ durchgeführt.

- $X$ hat die **Wertemenge** $\{0,1,\dots,n\}$ und die **Wahrscheinlichkeitsverteilung**

  $$
  \begin{pmatrix}
  0 & 1 & \dots & n \\
  p_0 & p_1 & \dots & p_n
  \end{pmatrix}
  $$

  mit :$$
  p_i = p(X = i) = \binom{n}{i} p^i (1 - p)^{n-i}, \quad (i = 1,2,\dots,n).
  $$
- Dabei gilt:

  $$
  \sum_{i=0}^{n} p_i = \sum_{i=0}^{n} \binom{n}{i} p^i (1 - p)^{n-i} = (p + (1 - p))^n = 1^n = 1
  $$

  *(Binomischer Satz)*

---
## Folgerung
mit: 
- unabhängige [[Bernoulli Verteilung|Bernoulli-verteilte]] Zufallsgrößen mit Parameter p

Ist $\mathcal{X}$ eine binomialverteilte Zufallsgröße  mit Parameter $p$ und Wertemenge $\{ 1,2,\dots,n \}$ dann gilt:
- $E(X)=E(\mathcal{X_{1}}+\mathcal{X_{2}}+\dots +\mathcal{X_{n}})=E(\mathcal{X_{1}})+\dots+E(\mathcal{X_{n}})$
- $E(\mathcal{X})=n\cdot p$

### Varianz
- $\text{Var}(X)=\text{Var}(\mathcal{X_{1}}+\mathcal{X_{2}}+\dots +\mathcal{X_{n}})=\text{Var}(\mathcal{X_{1}})+\dots+\text{Var}(\mathcal{X_{n}})$
- $\text{Var}(\mathcal{X})=np(1-p)$

[[Taylor Polynome]]

