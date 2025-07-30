Sei $\mathcal{M} = \langle Q, \Sigma, \Gamma, \delta, Q_0, F \rangle$ ein [[Kellerautomat PDA]]
Eine Konfiguration von $\mathcal{M}$ ist ein Tripel $\langle q,w,\gamma \rangle$
- $q \in Q$
- $w \in \Sigma^{*}$
- $\gamma \in \Gamma^{*}$

### Übergänge in Konfigurationen
Übergang von $\langle q,vw,\psi\gamma\rangle$in einer anderen Konfiguration $\langle q',w,\psi'\gamma\rangle$ falls:
- $\langle q',\psi' \rangle \in \delta(q,v,\psi)$
Diese Übergang wird wie gefolgt symboliziert:
-  $\langle q,vw,\psi\gamma\rangle \vdash \langle q',w,\psi'\gamma\rangle$

Der PDA M akzeptiert ein Wort w genau dann, wenn es eine Folge von Übergängen
$⟨q_{s}, w, ϵ⟩ ⊢^{*} ⟨q_{f} , ϵ, γ⟩$ für ein $q_{s} ∈ Q_{0}$ und $q_{f} ∈ F$ gibt

---

## Bemerkung
$\vdash ^{*}$ ist die *reflexive und transitive* Abschluss von $\vdash$

---
### Beispiel Übergangsfunktion 
$\langle q_{2},D \rangle \in \delta(q_{1},a,C)$
- Bedeutung : "Wenn der PDA im Zustand $q_{1}$ das Symbol **a** einliest und **C oben vom Keller nimmt** (pop), dann **kann er in den Zustand** $q_{2}$ **wechseln** und dabei **D auf den Keller legen** (push)"

$\langle q_{2},\epsilon \rangle \in \delta(q_{1},a,\epsilon)$
- "Wenn der PDA im Zustand $q_{1}$ das Symbol **a** einliest, dann kann er in den Zustand
$q_{2}$ wechseln und den **Keller unverändert lassen**."

$\langle q_{2},D \rangle \in \delta(q_{1},\epsilon,C)$
- Wenn der PDA im Zustand q1 das Symbol C oben vom Keller nimmt (pop), dann kann er in den Zustand q2 wechseln und dabei D auf den Keller legen (push), ohne ein Symbol zu lesen.

- erste ist kein Akzeptierende Lauf, da kein *S* liegt oben im [[Keller]]

![[Screenshot from 2024-12-14 19-27-00.png]]