
Eine Substitution ist eine endliche Menge der Form $\{x_{1} \mapsto t_{1}, . . . , x_{n} \mapsto t_{n} \}$
wobei $x_{1}, . . . , x_{n} ∈ V$ paarweise verschiedene Variablen und $t_{1}, \dots , t_{n} ∈ T$ beliebige Terme sind

- wenn man jedes freie Vorkommen einer Variablen $x_{i}$ in A simultan durch $t_{i}$ ersetzt
![[Pasted image 20250623184453.png]]

Eine Formel bzw. einen Term $A \sigma$, der durch Anwendung einer Substitution $\sigma$ auf A
entsteht, nennt man **Instanz von A** (*unter* $\sigma$)


## Komposition
Für Substitutionen $\sigma = \{x_{1}  \mapsto t_{1}, \dots , x_{n} \mapsto t_{n} \}$ und $\theta = {y_{1} \mapsto s_{1},\dots,  y_{m} \mapsto s_{m}}$ ist die Komposition $σ ◦ θ$ die folgende Substitution:
- $\{ x_{1} \mapsto t_{1}\theta, . . . , x_{n} \mapsto t_{n}\theta \} \cup \{ y_{i} \mapsto s_{i} | y_{i} ∈ {y_{1}, . . . , y_{m}} \backslash \{x_{1}, . . . , x_{n} \} \}$
- also man hängt Theta nach jede Substitution von $x$
- und ersetzt alle $y$ durch $s$, die **noch unverändert liegen** (also diejenige $y$ die von $x$ nicht verändert würden)

### Satz 
Für alle Terme oder Formeln A und Substitutionen $\sigma$ und $\theta$  gilt:
$$
A(\sigma \circ \theta) = (A\sigma)\theta
$$


---
## Allgemeine Substitutionen
Eine Substitution $\sigma$ ist genau dann **mindestens so allgemein** wie eine Substitution $θ$, in
Symbolen $σ ⪯ θ$, wenn es eine Substitution $λ$ gibt, so dass $σ ◦ λ = θ$