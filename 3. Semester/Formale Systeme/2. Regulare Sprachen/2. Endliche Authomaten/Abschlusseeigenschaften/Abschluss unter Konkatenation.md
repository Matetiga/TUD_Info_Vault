## Konkatenationsautomat $M_{1} \odot M_{2}$
mit: $M_{1}= \langle Q, \Sigma, \delta, Q_{0},F \rangle \text{ und } M_{2}= \langle Q_{2}, \Sigma, \delta_{2}, Q_{0,2},F_{2} \rangle$

- dann folgt: 
	- $\langle Q_{1} \cup Q_{2}, \Sigma, \delta, Q_{0,1},  F_{2}$
$$
\delta(q, a) = 
\begin{cases} \delta_1(q, a) & \text{falls } q \in Q_1, \\ \delta_2(q, a) & \text{falls } q \in Q_2.  \\
\end{cases}
$$
$$
\delta(q,\epsilon)=
\begin{cases}
Q_{0,2} \text{ falls } q \in F_{1} \\
\emptyset \text{ andersfalls}
\end{cases}
$$
**Alle Endzustände von $M_{1}$ werden zu alle Startzustände aus $M_{2}$ abbgebildet**

---
## Satz
Für alle [[2. Nichtdeterministische endliche Automaten NFA]] $M_{1}$ und $M_{2}$ folgt: 
- $L(M_{1} \odot M_{2})= L(M_{1}) \circ L(M_{2})$
![[IMG_2331.jpeg]]