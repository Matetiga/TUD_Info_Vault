Sei $(S; \circ)$ eine Permutationsgruppe auf der endlichen Menge $X$ und $x \in X$
$x^{S}:= \{  \alpha(x)|\alpha \in S \}$ wird die **Bahn** von $x$ unter (der Wirkung von) $S$ gennant 

<span style="color:#ffff00">Bahnen sind den Pfad, dass ein Element in der Permutationsgruppe macht</span>
#### Bemerkung 
- $x^{S} \subseteq X$
- **Bahnen bestehen** also aus solchen **Elementen der permutierenten Menge** $X$, die durch Elemente der Permutationsgruppe $S$ *aufeinander abgebildet werden können*

---

### Beispiel
$S=\{ (1),(12)(345),(345),(12),(354), (12)(354) \}$
- Bahnen: 
	- $1^{S}=2^{S}= \{ 1,2 \}$
	- $3^{S}=4^{S}=5^{S}=\{ 3,4,5 \}$

---

## Menge der Bahnen 
- Bildet eine **Zerlegung Z** von $X$
	- Jedes $x \in X$ ist in einer Bahn enthalten: $x=id(x) \in x^{S}$
	- Je zwei verschiedene Bahne sind disjunkt
	- Die Menge der Zerlegung der Bahnen von X zeigt **den Pfad jedes Element** in der Permutationsgruppe



---
Jede Permutationsgruppe $(S; \circ)$ bildet eine [[Äquivalenzrelationen]] $R_{\zeta}$ in $X$

- Seien $x,y \in X$
	- $(x,y) \in R \Leftrightarrow x^{S}=y^{S}$
	- x und y sind in derselben Bahn unter der Wirkung von S enthalten

[[Äquivalenzklassen]] von $R_{\zeta}$ in X sind:
- $[x]_{R_{\zeta}}=\{ y \in X | x^{S}=y^{S} \}=x^{S}$

[[Faktormenge]] von $X$ nach $R_{\zeta}$ ist: 
- $X/R_{\zeta}=\{ [x]_{R_{\zeta}} |x \in X\}=\{ x^{S}|x \in X \}$

