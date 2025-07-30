Das Minimalpolynom $m_{\alpha^n}(x)$ hat genau die Nullstellen, die zur gleichen **Minimalzyklotomischen Klasse** gehören wie $\alpha^n$ Die Minimalzyklotomische Klasse von $\alpha^n$ ist: ([[Zyklotome Klasse]])

mit [[Körper]] $K=GF(p^{k})$
- $n \in \mathbb{N}$
- Minimalzyklotomische Klasse: $Kl(\alpha^{n})=\{ \alpha^{n\cdot p^{0}},\alpha^{n\cdot p^{1}},\alpha^{n\cdot p^{2}},\dots \} \text{ mod }p^{k}-1$

### Besimmung der Minimalpolynom
Aus der Elemente der Minimalzyklotomische Klasse lässen sich die Elemente des Minimalpolynoms ablesen:
- $m_{\alpha^{n}}=(x-\alpha^{n})(x-\alpha^{n\cdot p})\dots$

---

## Beispiel
mit: $K=GF(25)=GF(5^{2})$
- ist $x-\alpha^{17}$ Teiler von $m_{\alpha^{2}}$?

somit folgt die Minimalzyklotomische Klasse: 
- $Kl=\{ \alpha^{2},\alpha^{2\cdot 5},\alpha^{2\cdot 5^{2}},\dots  \} \text{ mod } 5^{2}-1=\{ 2,10 \}$
- somit ist $\implies m_{\alpha^{2}}=(x-\alpha^{2})(x-\alpha^{10})$

also : -  $x-\alpha^{17}$  kein Teiler von $m_{\alpha^{2}}$