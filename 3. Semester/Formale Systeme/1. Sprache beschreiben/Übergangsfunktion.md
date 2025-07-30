### Beispiel
Angenommen, wir haben einen [[2. Nichtdeterministische endliche Automaten NFA]] mit den Zuständen $( Q = \{q_0, q_1, q_2\} )$ und dem Alphabet $( \Sigma = \{a, b\} )$. Die Übergangsfunktion$( \delta )$ könnte wie folgt definiert sein:
- $\delta(q_0, a) = \{q_0, q_1\})$: 
	- Wenn der Automat im Zustand $( q_0 )$ ist und ein $a$ liest, kann er entweder im Zustand $q_{0}$ bleiben oder in den Zustand $q_{1}$ übergehen.
-  $( \delta(q_1, b) = \{q_2\} )$:
	- Wenn der Automat im Zustand $q_{1}$ ist und ein $b$ liest, wechselt er in den Zustand $q_{2}$

---

#### Wichtig 
- Ein [[1. deterministische Endliche Automaten DFA]] hat nur für einen Symbol und ein Zustand **genau ein Endzustand** 
- Ein [[2. Nichtdeterministische endliche Automaten NFA]] kann gleichzeitg **mehrere Endzustände** haben 
	- Eingabesymbole können **kein Endzustand** haben
	-  können **Übergänge haben, die kein Eingabesymbol brauchen** ($\epsilon-$Übergänge )
##### $\delta(R,av)= \delta(\delta(R,a)v)$
