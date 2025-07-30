Ein Lauf eines [[2. Nichtdeterministische endliche Automaten NFA]] $M= \langle Q, \Sigma, \delta, Q_{0},F \rangle$ für ein Wort $w=\sigma_{1},\dots,\sigma_{n}$ ist eine Folge von Zuständen $q_{0},\dots,q_{m}$ so dass gilt:
- $m$ Länge der Zustanden und $n$ Länge des Wörtes
- $q_{0} \in Q_{0}$
- $q_{i+1} \in \delta(q_{i},\sigma_{i+1})$ für alle $0\leq i<m$
- $m=|w|=n$
	-  oder $m<n$ und $\delta(q_{m},\sigma_{m+1})=\emptyset$
	- dann gibt ein **kein Zustand** von $q_{m}$ aus $\sigma_{m+1}$

### Lauf heißt: 
- **akzeptierend** falls: $m=n$ und $q_{n}\in F$
- **verwerfend** sonst

---

- [[1. deterministische Endliche Automaten DFA]] hat **genau einen Lauf** für jedes Wort
	- akzeptiert, wenn Lauf akzeptierend ist
- [[2. Nichtdeterministische endliche Automaten NFA]] hat **mehrere Läufe** für ein Wort
	- akzeptiert, wenn Lauf akzeptierend ist
