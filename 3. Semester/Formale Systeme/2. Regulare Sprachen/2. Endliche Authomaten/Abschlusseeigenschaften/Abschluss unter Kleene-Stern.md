Sei $M= \langle Q, \Sigma, \delta, Q_{0},F \rangle$. Der Automat $M^{*}$ ist ein $\epsilon \text{-NFA}$ ([[2. Nichtdeterministische endliche Automaten NFA]]) gegeben durch $\langle Q', \Sigma , \delta', Q_{0}', F' \rangle$ wobei:
- $Q'=Q \cup \{ q_{\epsilon} \}$ und $q_{\epsilon} \not \in Q$
- $\delta'(q,a)=\delta(q,a)$ für alle $q \in Q, a \in \Sigma$ und $\delta'(q_{f},\epsilon)=Q_{0} \forall q_{f} \in F$
- $Q_{0}'=Q_{0} \cup \{  q_{\epsilon} \}$
- $F_{0}'=F_{0} \cup \{  q_{\epsilon} \}$

---

## Satz
$$
L(M^{*})=L(M)^{*}
$$