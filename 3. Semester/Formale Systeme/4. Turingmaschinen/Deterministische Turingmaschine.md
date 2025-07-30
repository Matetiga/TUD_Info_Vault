#### Designentscheidungen
- Haben eine endliche Steuerung 
	- enldiche Zustände
- Unbeschränke Menge an Speicher
-  Die TM kann in jedem Schritt ein Zeichen aus dem Speicher lesen und eines schreiben (wie bei PDA)

---

## Definition 
Eine (deterministische) Turingmaschine (DTM) ist ein Tupel $\mathcal{M} = \langle Q, \Sigma, \Gamma, \delta, q_0, F \rangle$ mit den folgenden Bestandteilen:

- $Q$: endliche Menge von **Zuständen**  
- $\Sigma$: **Eingabealphabet**  
- $\Gamma$: **Arbeitsalphabet** mit $\Gamma \supseteq \Sigma \cup \{ \textvisiblespace \}$  
	- $\textvisiblespace$ als ein Blank Space
- $\delta$: **Übergangsfunktion**, eine partielle Funktion  
	- $\delta: Q \times \Gamma \to Q \times \Gamma \times \{L, R, N\}$
- $q_0$: **Startzustand** $q_0 \in Q$  
- $F$: Menge von akzeptierenden **Endzuständen** $F \subseteq Q$

---
### Erklärung Übergangfunktion:
$\delta(q, a) = \langle p, b, D \rangle$:  
„Liest die Turingmaschine (TM) in Zustand $q$ unter dem Lese-/Schreibkopf ein $a$,  
dann wechselt sie zu Zustand $p$, überschreibt das $a$ mit $b$  
und verschiebt den Lese-/Schreibkopf gemäß $D \in \{L, R, N\}$  
(nach links, nach rechts, gar nicht).“

---

#### Beispiel
![[Screenshot from 2025-01-09 14-18-39.png]]