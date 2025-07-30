
## Übergangswahrscheinlichkeit $p(x_{j}|x_{i})$:
#### Die Wahrscheinlichkeit der Zustand $x_{j}$, wenn der Zustand $x_{i}$ vorliegt

$$
\begin{array}{c}
p(x_{j}|x_{i})=
\end{array}
\begin{pmatrix}
p(x_{1}|x_{1}) & p(x_{2}|x_{1})\\ \\
p(x_{1}|x_{2}) &p(x_{2}|x_{2})
\end{pmatrix}
$$

$$
p(x_{i}|y_{j})=\frac{p(x_{i},y_{j})}{p(y_{i})}
$$

---
### Beispiel:
SPASSSPASSSPASS

$N=3\quad x \{A,P,S\}$

=> Man untersucht mit welcher Wahrscheinlichkeit eine Buschsabe nach einer anderen vorkommt.

|         | x_1 = A | x_2 = P | x_3 = S |
| ------- | ------- | ------- | ------- |
| x_1 = A | -       | -       | 3 Mal   |
| x_2 = P | 3 Mal   | -       | -       |
| x_3 = S | -       | 3 Mal   | 5 Mal   |

![[WhatsApp Image 2024-04-26 at 19.43.25 1.jpeg]]

### Dies folgt zu dieser Matrix:
$$
\begin{bmatrix}
0 & 0 & 1 \\
1 & 0 & 0 \\
0 & \frac{3}{8} & \frac{5}{8}
\end{bmatrix}
$$
oder auch: 

|     | A   | P   | S   |
| --- | --- | --- | --- |
| A   | 0   | 0   | 1   |
| P   | 1   | 0   | 0   |
| S   | 0   | 3/8 | 5/8 |


