## Definition
$$
\begin{align*}
& \text{Zufallsgrößen } X_1, X_2, \dots, X_n \text{sind unabhängig }  \\
  &  \Leftrightarrow  \\
& p(X_1 = x_1, X_2 = x_2, \dots, X_n = x_n) = p(X_1 = x_1) \cdot p(X_2 = x_2) \cdots p(X_n = x_n)

\end{align*}
$$

für alle $(x_1, x_2, \dots, x_n)$.

---

### Bemerkung
$$
E(\alpha_1 X_1 + \dots + \alpha_n X_n) = \sum_{\omega \in \Omega} (\alpha_1 X_1(\omega) + \dots + \alpha_n X_n(\omega)) \cdot p(\omega)
$$
$$
= \alpha_1 \sum_{\omega \in \Omega} X_1(\omega) p(\omega) + \dots + \alpha_n \sum_{\omega \in \Omega} X_n(\omega) p(\omega)
$$

$$
= \alpha_1 E(X_1) + \dots + \alpha_n E(X_n)
$$

---

## Satz
Für **unabhängige** Zufallsgrößen gilt:

$$
\operatorname{Var}(X_1 + X_2 + \dots + X_n) = \operatorname{Var}(X_1) + \operatorname{Var}(X_2) + \dots + \operatorname{Var}(X_n)
$$
