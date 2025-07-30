Für ein **NFA** $M= \langle Q, \Sigma, \delta, Q_{0},F \rangle$ definieren wir die **Potenzmenge-DFA** wie gefolgt:
$M_{DFA}= \langle Q_{DFA}, \Sigma, \delta, Q_{DFA},F_{DFA} \rangle$
- $Q_{DFA}$ **Potenzmenge** von Q ($2^{Q}$)
- $\delta_{DFA}(R,a)= \bigcup_{q \in R} \delta(q,a)$
- $q_{0}=Q_{0}$  : **Startzustand**
- $F_{DFA}=\{ R \in 2^{Q}| R \cap F \neq \emptyset \}$: jede Menge, die **zumindest ein Endzustand** hat


### Wichtig zur Aufstellen 
Start Zustand der Potenzmenge ist die Menge aller Startzustände 
Ein Zustand in der Potenzmenge wird ein Endzustand, wenn mindestens ein Endzustand in der Menge gibt 

---

## Satz Robin/Scott
- $L(M)=L(M_{DFA})$ da:
$$
\begin{gather}
w \in L(M) &\Leftrightarrow & \delta(Q_{0},w) \cap F \neq \emptyset\\
&\Leftrightarrow & \delta_{DAF}(Q_{0},w) \cap F \neq \emptyset\\ 
&\Leftrightarrow & \delta_{DAF}(Q_{0},w) \in F_{DAF}\\ 
&\Leftrightarrow & w \in L(M_{DAF})\\
\end{gather}
$$
- $\delta_{DFA}(R,a)=\delta(R,a)$
### Beispiel
- mit : $\{ 1 \}^{*} \circ \{ \{ 0 \} \circ \{ 1 \}^{+} \}^{*}=(\{ 0 \} \circ \{ 1 \} \cup \{ 1 \})^{*}$
- das Diagram lässt sich vereinfachen indem man folgendes macht:
	- $q_{1}$ ist unerreichbar
	- $\emptyset$ ist irrelevant auch für akzeptierende Läufe, da es nicht verlassen sein kann 
![[Screenshot from 2024-10-25 18-29-07.png]]