Gegeben zwei [[2. Nichtdeterministische endliche Automaten NFA]] mit 
- $M_{1}= \langle Q, \Sigma, \delta, Q_{0},F \rangle$
- $M_{2}= \langle Q_{2}, \Sigma, \delta_{2}, Q_{0,2},F_{2} \rangle$

### Vereinigungsautomat $M_{1} \oplus M_{2}$
mit : $\langle Q_{1} \cup Q_{2}, \Sigma, \delta_{12}, Q_{0,1} \cup Q_{0,2}, F_{1} \cup F_{2}$
- **also, zwei Automaten in einem einzigen verbinden**
falls: 
$$
\delta_{12}(q, a) = 
\begin{cases} \delta_1(q, a) & \text{falls } q \in Q_1, \\ \delta_2(q, a) & \text{falls } q \in Q_2.  \\
\end{cases}
$$


---
## Satz
$$
L(M_{1}\oplus M_{2})=L(M_{1}) \cup L(M_{2})
$$

