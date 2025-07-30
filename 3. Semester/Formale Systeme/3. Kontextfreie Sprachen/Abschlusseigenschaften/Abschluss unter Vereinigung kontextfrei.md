zwei Gramatiken 
- $G_{1}= \langle V_{1},\Sigma,P_{1},S_{1} \rangle$
- $G_{2}= \langle V_{2},\Sigma,P_{2},S_{2} \rangle$
- mit $V_{1} \cap V_{2}= \emptyset$

## Vereinigungsgramatik
$G_{1} \biguplus G_{2}:=⟨V_{1} ∪ V_{2} ∪ {S}, Σ, P_{1} ∪ P_{2} ∪ {S → S_{1} | S_{2}}, S⟩,$

#### Satz
$L(G_{1} \biguplus G_{2}) = L(G_{1}) ∪ L(G_{2})$

---
### Wichtig 
Wenn $G_{1}$ und $G_{2}$ von Typ $i ∈ {2, 1, 0}$ sind, dann ist auch $G1 \biguplus G2$ von Typ $i$
- also wenn man beim Vereinigungsgramatik **zwei Gramatiken mit dem selben Typ** vereinigt, dann ist die Endgramatik **wieder von selben Typ**