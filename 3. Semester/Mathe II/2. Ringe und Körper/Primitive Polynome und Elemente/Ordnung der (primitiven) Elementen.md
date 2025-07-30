mit:
- $K=\mathbb{Z}_{3}[x] / f(x)$
- $f(x)=x^{2}+x+2$ irreduzibel und primitiv ([[Bestimmung ob f(x) primitiv]])
- Aus [[Anzahl Primitive Elemente]] folgt:
	- $\phi(8)=4$
	- die Elemente sind wie gefolgt:
		- [[Primitives Element]] $=\{ x,x^{3},x^{5},x^{7} \}$
			- $x \equiv x$
			- $x^{3}\equiv2x+2$
			- $x^{5}\equiv2x$
			- $x^{7} \equiv x+1$

## Ordnung der Elemente
- mit: $a^{k} \in \mathbb{Z}_{3}[x] / f(x)$
$$
\text{Ord}(a)=\frac{|K^{*}|}{\text{ggT}(k,|K^{*}|)}
$$
### Beispiele:
Ordnung von $(x+1)$ 
- mit $x^{7}=(x+1)$ [[Primitives Element]], da es die Ganze Grupper erzeugt
- $k=p-1 \text{ aus }a^{p-1}\equiv 1$
	- $\text{Ord}(x+1)= \frac{|K^{*}|}{\text{ggT}(7,8)}=8$

Ordnung von $(x+2)$
- mit : $x^{6} \equiv x+2$
	- $\text{Ord}(x+2)= \frac{8}{\text{ggT}(6,8)}= \frac{8}{2}= 4$
