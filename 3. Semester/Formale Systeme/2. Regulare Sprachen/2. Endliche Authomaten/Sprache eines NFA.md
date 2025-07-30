### NFA können nur reguläre Sprachen akzeptieren
- [[Typ 3]]
- Sprache eines NFA  Menge aller Wörter  für die  ein akzeptierende Lauf  (Läufe eines NFA ) hat 
- [[2. Nichtdeterministische endliche Automaten NFA]]

- $L(M)=\{ w \in \Sigma^{*}| \delta(Q_{0},w) \cap F \neq \emptyset \}$
	- Die Bedingung : $\delta(Q_{0},w) \cap F \neq \emptyset \}$ bedeutet: *Mindestens einer der Zustände , die man durch einlesen von $w$ von einem Startzustand aus erreichen kann, ist ein Endzustand*
