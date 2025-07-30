## Dient zur Bestimmung des Multiplikativen Inverses
-  [[Einheit]] und *Multiplikativen Inverses* 

---
## Bestimmung Für [[Polynomringe modulo f(x)]]
mit: 
- $\mathbb{Z}_{n}[x] / f(x)$
- $p(x) \in \mathbb{Z}_{n}[x] / f(x)$
#### Voraussetzung
 $\text{ggT}(f(x),p(x))=1 \Leftrightarrow \text{ Mult. Invers existiert}$

#### Schritte 
1) $f(x)=q_{1}(x)\cdot p(x)+r_{1}(x)$
2) $p(x)=q_{2}(x)\cdot r_{1}+r_{2}(x)$
3) Wiederhole folgedes bis :  $r_{k+1}(x)=0$
	- $r_{k-1}=q_{k}\cdot r_{k}+r_{k+1}$
<span style="color:#ffff00">Der letzte Rest ungleich Null ist der ggT, also 1</span> 
4) Dann folgt das Multiplikatives Invers $\implies r_{k+1}=1=r_{k-1}-q_{k}\cdot r_{k}$

---

### Beispiel
mit:
- $p(x) = x^3 + x + 1$.
- $\mathbb{Z}_{2}[x] / x^{3}+ x^{2}+1$

1. **Falls Invers Existiert, muss folgendes gelten:** 
   $\text{ggT}(f(x), p(x)) = 1$  

2. **Erweiterter euklidischer Algorithmus**:  
- mit $q_{1}(x)=x$
-  $x^3 + x^2 + 1 \div (x^2 + x + 1)$ $=x$ und den *Rest* $r_1(x) = x + 1$. 

- mit $q_{2}(x)=x$
-  $x^2 + x + 1 \div (x + 1)$ $=x$ und den *Rest* $r_2(x) = 1$

somit folgt: 
$f(x)=q_{1}\cdot p(x)+r_{1}(x)$
$p(x)=q_{2}\cdot r_{1}(x)+r_{2}(x)$
- und :
	- $r_{2}(x)=1=p(x)-q_{2}(x)\cdot r_{1}(x)$
	- nach Umformungen : $1 \equiv (1+q_{1}\cdot q_{2}) \cdot p(x)$
$p(x)^{-1} \equiv 1 + x^2 \mod f(x)$


---

## Bestimmung mult. Invers in einer Gruppe $\mathbb{Z}_{n}$
Multiplikatives Invers existiert falls: 
- $\text{ggT}(x,y)=1$

somit folgt:
- $\text{ggT}(x,y)=1=a \cdot x+b\cdot y$

### Beispiel
Finde das multiplikatives Invers von 10 in $\mathbb{Z}_{101}$
- angenommen : $\text{ggT}(10,101)=1$
somit folgt: 
$$
\begin{align}
1=\ &  a\cdot 10+ b \cdot 101 \\
\text{ mit : } 101= \ &10\cdot 10 +1 \\
\text{ somit folgt: } 1= \ & -10 \cdot 10 + 1 \cdot 101
\end{align}
$$
- dann *sucht man das Invers* von $-10$
	- $-10+101 \equiv 91 (mod \ 101)$

- somit ist : $10^{-1} \equiv 91$
