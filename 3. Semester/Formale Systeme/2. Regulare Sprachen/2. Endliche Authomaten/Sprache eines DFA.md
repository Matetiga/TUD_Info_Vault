### DFA können nur reguläre Sprachen akzeptieren
- [[Typ 3]]

Fällt in der Klasse der **regulären Sprachen** rein
## Erweiterung mit Übergangsfunktion
$$
\delta^{*}:Q \times \Sigma\to Q
$$

Für ein Zustand $q \in Q$ und ein Wort $m \in \Sigma^{*}$ sei:
$\delta^{*}(q,w)$ **der eindeutig bestimmte Zustand**, den man erreicht, wenn man ausgehend von $q$ das Wort $w$ einliest 
- $\delta^{*}(q,\epsilon)=q$ mit $w=\epsilon$ 
- $\delta^{*}(q,av)=\delta^{*}(\delta(q,a)v)$ mit $w=av$ 

Wert ist undefiniert, wenn der nötgen Übergänge undefiniert ist

---
## Definition
Die Sprache eines DFA $M= \langle Q, \Sigma, \delta, q_{0},F \rangle$ ist die Menge: 
- $L(M)=\{ w \in \Sigma^{*}| \delta^{*}(q_{0},w) \in F \}$