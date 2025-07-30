## Beispiel
mit: 
- $K=\mathbb{Z}_{5}[x] / f(x)$
- $f(x)=x^{2}+x+2$  [[Irreduzibel Polynom]]
- $|K|=5^{2}=25$ [[Anzahl Elemente eines Körpers Z_p]]
- $|K^{*}|=5^{2}-1=24 \text{ da Null entfernt wird}$ 
	- ($K^{*}$ = *Multiplikative Gruppe*) 

Nach [[Satz von Lagrange - Ordnung Untergruppe]] folgt:
- $|\langle x\rangle| \text{ teilt } K^{*}$

### Bestimmung der Logarithmentaffel
$f \text{ primitiv } \Leftrightarrow x^{k} \neq 1$  für **alle echte Teiler von 24**, also:  $k\in \{ 1,2,3,4,6,8,12 \}$
- dann muss man das für jeden **Teiler einzeln probieren**

$\implies x \neq 1$

$\implies f(x)=x^{2}+x+2=0$
- $x^{2}=-x-2$
- $x^{2} \equiv 4x +3$

$\implies x^{3}=x^{2}\cdot x$
- $x^{3}=(4x+3)\cdot x$
- $x^{3}=4x^{2}+3x$
- $x^{3}=4(4x+3)+3x$
- $x^{3}=x+2+3x$
- $x^{3}=4x+2$

$\implies x^{4}=x^{3}\cdot x$
- $x^{4}=(4x+2)\cdot x$
- $x^{4}=3x+2$

$\implies x^{6}=x^{4}\cdot x^{2}$
- $x^{6}=2$

$\implies x^{8}=(x^{4})^{2}$
- $x^{8}=3x+1$

$\implies x^{12}=(x^{6})^{2}$
- $x^{12}=4$

Somit würde gezeigt, dass $f(x)$ **primitiv ist**