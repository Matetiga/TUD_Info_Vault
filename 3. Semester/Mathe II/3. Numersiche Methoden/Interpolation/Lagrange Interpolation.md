## Lagrange Polynom 
$$p(x) = \sum_{k=0}^n a_k \cdot L_k(x)$$

mit: 
$$L_{k}(x)=\prod^{n}_{i=0;i \neq k} \frac{x-x_{i}}{x_{k}-x_{i}}$$
also:
$$L_{k}(x)=\frac{(x-x_{0})* \dots * (x-x_{k-1})(x-x_{k+1})* \dots * (x-x_{n})}{(x_{k}-x_{0})* \dots *(x_{k}-x_{k-1})(x_{k}-x_{k+1})* \dots *(x_{k}-x_{n})}$$
---
## Wert der Lagrange Polynome 
Lagrange Polynome sind linear unabhängig

$$L_k(x_i) =
\begin{cases}
1, & \text{wenn } i = k \\
0, & \text{wenn } i \neq k
\end{cases}
\quad \text{d.h. } i \in \{0, \dots, k-1\} \cup \{k+1, \dots, n\}
$$

---
