## Definition
Die O-Notation  charakterisiert Funktionen nach ihrem **asymptotischen Verhalten** und „versteckt“ lineare Faktoren

Für Funktionen $f , g : \mathbb{N} → \mathbb{R}$ schreiben wir genau dann $f ∈ O(g)$, wenn gilt:
- es gibt eine Zahl $c > 0$ und eine Zahl $n_{0} \in \mathbb{N}$
- sodass für jedes $n_{0}$ gilt: $f(n) \leq c \cdot g(n)$
- also : *f wächst höchstens so schnell wie g*

### Beispiel
- $10n^{3} + 42n^{2} -n+ 100 \in O(n^{3})$
- $2^{n} + n^{2000} \in O(2^{n})$
- $2^{721} \in O(1)$

---

## Schwestern der O-Notation
![[Pasted image 20250505095159.png]]