zwei Gramatiken 
- $G_{1}= \langle V_{1},\Sigma,P_{1},S_{1} \rangle$
- $G_{2}= \langle V_{2},\Sigma,P_{2},S_{2} \rangle$
- mit $V_{1} \cap V_{2}= \emptyset$

## Konkatention 
$G1 ◦ G2 = ⟨V_{1} ∪ V_{2} ∪ {S}, Σ, P_{1} ∪ P_{2} ∪ {S → S_{1}S_{2}}, S⟩$

#### Satz
Wenn $G_{1}$ und $G_{2}$ **kontextfrei sind**, dann ist $L(G_{1} ◦ G_{2}) = L(G_{1}) ◦ L(G_{2})$
Zudem ist $G_{1} ◦ G_{2}$ in diesem Fall kontextfrei
- wenn beide Gramatiken **nicht vom selben Typ** sind, dann ist **gilt das nicht**

![[Screenshot from 2024-12-09 11-35-29.png]]