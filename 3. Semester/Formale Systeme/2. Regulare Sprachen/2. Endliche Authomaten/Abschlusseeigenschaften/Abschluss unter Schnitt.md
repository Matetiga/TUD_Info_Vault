## Produktautomat $M_{1} \otimes M_{2}$
mit: $M_{1}= \langle Q, \Sigma, \delta, Q_{0},F \rangle \text{ und } M_{2}= \langle Q_{2}, \Sigma, \delta_{2}, Q_{0,2},F_{2} \rangle$

- dann folgt: $\langle Q_{1} \times Q_{2}, \Sigma, \delta_{12}, Q_{0,1} \times Q_{0,2}, F_{1} \times F_{2}$
- wobei: $\delta(\langle q_{1},q_{2} \rangle, a)= \delta_{1}(q_{1},a) \times \delta(q_{2},a)$

---

## Satz
$$
L(M_{1} \otimes M_{2})=L(M_{1})\cap L(M_{2})
$$
- Man erreicht ein Endzustand bei $M_{1} \otimes M_{2}$ **nur wenn, man ein Endzustand** bei $M_{1}$ und $M_{2}$ erreicht 
- falls $| A|=|B|=1 \Leftrightarrow | A\times B|=1$ 
	- dann ist der Produktautomat von DFAs auch ein [[1. deterministische Endliche Automaten DFA|DFA]]
	
![[IMG_2329.jpeg]]