## Beweis 
- Durch reduktion auf einem [[Kontextfreie Sprachen|Kontextfreie Grammatik]]-Schnittproblem ([[Unentscheidbare Probleme]]) 

1. Wir Konstruieren aus $G_{1}$ und $G_{2}$ eine logische Theorie $\mathcal{T}$ mit den folgenden Sätze:
- Ein Produktionsregel $A\to\sigma_{1}, \dots, \sigma_{n}$ von $G_{1}$ und $G_{2}$
- $∀x_{0}, . . . , x_{n}.( p_{σ1} (x_{0}, x_{1}) ∧ . . . ∧ p_{σn} (x_{n−1}, x_{n})) \to p_{A}(x_{0}, x)$
	- Das bedeutet, dass das Nichtterminalsymbol A sich in eine Kette von $\sigma_{1}, \dots, \sigma_{n}$ kodieren lässt und abkürzen in $p_{A}(x_{0}, x)$ (*erste und letzte Symbol der Kette*)


2. Seien $S_{1}$ und $S_{2}$ die *Startsymbole* von $G_{1}$ und $G_{2}$.  
 Dann wollen wir das Schnittproblem kodieren, indem wir fragen, ob die folgende Formel folgt:
 - $∃x, y.( p_{S_{1}} (x, y) ∧ p_{S_{2}} (x, y))$
 - also: es existieren Startsymbole, die in zwei Wörter dieselben sind
 - *Es kann auch Interpretationen geben, welche keine Kodierung von $w$ enthalten*

3. Alle möglichen Wörter müssten kodiert vorkommen . . . 
Dazu fügen wir noch folgende Sätze hinzu: 
- $∀x.∃y.p_{a}(x, y)$ für jedes *Terminalsymbol* a
- So stellt man sicher sein, dass jede Kette eine gültige Darstellung hat 

4. Dann gilt: 
$$
\mathcal{T} \models ∃x, y.( p_{S_{1}} (x, y) ∧ p_{S_{2}} (x, y)) \text{ genau dann, wenn } w \in L(G_{1}) \cap L(G_{2})
$$ 

[[Resolution]]