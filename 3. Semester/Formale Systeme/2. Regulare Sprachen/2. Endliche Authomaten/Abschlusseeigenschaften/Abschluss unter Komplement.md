Ein [[1. deterministische Endliche Automaten DFA]] wird komplementiert, indem man die **akzeptierende und verwefende  Zustände vertauschen** 

somit folgt:
$$
\text{ DFA } M= \langle Q, \Sigma, \delta, Q_{0},F \rangle \text{ dann ist der } \bar{M} \text{ DFA } = \langle Q, \Sigma, \delta, Q_{0},Q \setminus F \rangle
$$
-  mit $Q \setminus F$ -> $Q$ ohne $F$
![[IMG_2330.jpeg]]


### DFA mit totaler [[Übergangsfunktion]]
- dann folgt das nächste Zusammenhang
$$
L(\overline{M})= \overline{L(M)}
$$