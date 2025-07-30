#### (Mit der Produktregel)

$$
\int (u'(x)\cdot v(x)+u(x)\cdot v'(x)) \, dx =u(x)\cdot v(x)+c
$$

#### Das Integral lässt sich trennen
$$
\begin{gather}
\int  u'(x)\cdot v(x) \, dx  + \int u(x)\cdot v'(x)  \, dx =u(x)\cdot v(x)+c\\
\int u'\cdot v \, dx = u\cdot v-\int u\cdot v' \, dx\\
\int u\cdot v' \, dx = u\cdot v-\int u'\cdot v \, dx
\end{gather}
$$

---

## Beispiel
### Mit Hilfe des oberen Zusammenhänges
- x => u
- cos(x) => v'
- 1 => u'
- sin(x) => v
$$
\begin{gather}
\int x\cdot \cos(x) \, dx =x\cdot \sin(x)-\int 1\cdot \sin(x) \, dx \\
=x\cdot \sin(x)+\cos(x)+c
\end{gather}
$$![[WhatsApp Image 2024-06-21 at 11.15.17.jpeg]]