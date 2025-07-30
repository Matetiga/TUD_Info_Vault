## Voraussetzungen 
##### f und g sind auf dem Intervall $(a,b)$ *2-mal stetig differenzierbar* (2-mal differenzierbar mit stetigen Ableitungen)

$x_{0}\in (a,b), \quad f(x_{0})=g(x_{0})=0$

---
## Regeln 
### 1. (Gilt für Grenzwerte: $\frac{0}{0} \text{ bzw. } \frac{\pm\infty}{\pm\infty}$)
$$
\lim_{  x \to x_{0} } \frac{f(x)}{g(x)}= \frac{f'(x)}{g'(x)} 
$$
#### Bemerkung : 
- **NICHT nach QUOTIONTREGEL** ableiten
	- man leitet die Funktionen individuell ab
- Es ist möglilch, dass $\lim \frac{f(x)}{g(x)}$ **existiert** und $\lim \frac{f'(x)}{g'(x)}$ **nicht**



### 2. Für Grenzwerte: $0\cdot(\pm \infty)$
$$
\lim f(x)\cdot g(x)^{0\cdot(\pm \infty)}=\lim \frac{f(x)}{\frac{1}{g(x)}}^ {\frac{0}{0}}=\lim \frac{g(x)}{\frac{1}{f(x)}}^ {\frac{\infty}{\infty}}
$$
### Für Grenzwerte: $0^{0}, 1^{\infty}$
#### mit e:
$$
\begin{align}
\lim f(x)^{g(x)^{0^{0}}}=\lim e^{\ln f(x)^{g(x)}} \\
=\lim e^{g(x)\cdot \ln f(x)} \\
=e^{\lim g(x)\cdot \ln f(x)}
\end{align}
$$
#### MIT : $f(x)>0$

---
