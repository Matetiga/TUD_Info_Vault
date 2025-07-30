## Quantifizierte Boolsche Formel
Jede QBF-Formel $Q$ wird ein eindeutiger Wahrheitswert $W(Q)$ zugeordnet
- $W(∃p.F[p]) = 1 \text{ falls } W(F[p/⊤]) = 1 \text{ oder } W(F[p/⊥]) = 1$
- $W(\forall p.F[p]) = 1 \text{ falls } W(F[p/⊤]) = 1 \text{ oder } W(F[p/⊥]) = 1$
$\phi [p / \top ]$beduetet : $\phi$ mit $p$ ersetz durch $\top$ bzw. $\bot$ 

Eine logische Fomel der folgenden Form:
- $Q_{1}p_{1}.Q_{2}p_{2}.\dots.Q_{l}p_{l}.F[p_{1},\dots,p_{l}]$
- mit $i\geq 0 ; \quad Q_{i} \in \{ \exists ,\forall \}$
- $F$ ist eine aussagenlogische Formel mit $p_{i}$ Atome

### Beispiel
$\forall p.\exists q.(p \to q) \land (q \to p)$
- for all $p$ existiert ein $q$ mit der Formel...

![[Pasted image 20250519115313.png]]