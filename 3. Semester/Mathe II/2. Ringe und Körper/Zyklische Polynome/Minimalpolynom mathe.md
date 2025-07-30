# Definition
- Sei $GF(p^t)$ ($p$ prim, $t \in \mathbb{N}$, $t > 1$) ein endlicher Körper 
- $\alpha$ eine [[primitiven n-ten Einheitswurzel]] in $GF(p^t)$.

Betrachtet wird ein Element $\alpha^i \in GF(p^t)$.

Das **Minimalpolynom** $m_{\alpha^i}(x)$ von $\alpha^i$ ist das **normierte** *Polynom kleinsten Grades* in $GF(p)[x]$, das $\alpha^i$ als Nullstelle hat.

---
## Bemerkungen

1. **Bemerkung**: Betrachtet wird der Polynomring $GF(p^t)[x]$. Es gilt:
   $$
   GF(p)[x] \nsubseteq GF(p^t)[x]
   $$
   
2. **Bemerkung**: Für jedes $\alpha^i$ existiert ein Minimalpolynom.
3. **Bemerkung**: Normierte Polynome haben den höchsten Koeffizienten $1$:
   $$
   x^k + a_{k-1}x^{k-1} + \dots + a_1x + a_0.
   $$
   
4. **Bemerkung**: Für jedes $\alpha^i$ ist das Minimalpolynom **eindeutig bestimmt**.

---

### Eigenschaften Minimalpolynom $m_{\alpha^{i}}(x)$
- $m_{\alpha^{i}}(x)$ hat den höchsten Koeffizient 1 
- $m_{\alpha^{i}}(x)$ hat minimalen Grad bzgl. folgende Eigenschaften:
