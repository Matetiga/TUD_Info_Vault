Zur Vereinfachung der folgenden Definition schreiben wir $\Sigma_\epsilon$ für $\Sigma \cup \{\epsilon\}$ (analog für $\Gamma_\epsilon$)
Als [[2. Nichtdeterministische endliche Automaten NFA|NFA]] definiert

---
## Definition
Ein **Kellerautomat** (international: „PDA“, „Pushdown Automaton“) $\mathcal{M}$ ist ein Tupel  
$\mathcal{M} = \langle Q, \Sigma, \Gamma, \delta, Q_0, F \rangle$ mit den folgenden Bestandteilen:

- $Q$: endliche Menge von **Zuständen**  
- $\Sigma$: **Eingabealphabet**  
- $\Gamma$: **Kelleralphabet**  
- $\delta$: **Übergangsfunktion**, eine ==totale Funktion==  
	- $\delta: Q \times \Sigma_\epsilon \times \Gamma_\epsilon \to 2^{Q \times \Gamma_\epsilon}$
	- wobei $2^{Q \times \Gamma_\epsilon}$ die Potenzmenge von $Q \times \Gamma_\epsilon$ ist.
- $Q_0$: Menge möglicher **Startzustände** $Q_0 \subseteq Q$  
- $F$: Menge von **Endzuständen** $F \subseteq Q$

##### Wir wollen erlauben, . . .
(1) . . . dass der Automat manchmal kein Eingabesymbol liest (ϵ-Übergänge);
(2) . . . dass der Automat manchmal kein Kellersymbol liest;
(3) . . . dass der Automat manchmal nichts auf den Keller schreibt

---
