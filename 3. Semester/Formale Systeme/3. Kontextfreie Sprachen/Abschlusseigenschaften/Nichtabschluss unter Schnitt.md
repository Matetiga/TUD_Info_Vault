### Wichtig:
Es **bedeutet nicht direkt**, dass Schnitte bei kontextfreien Sprachen *immer nicht kontextfrei sein können*

## Satz 
es gibt **kontextfreie** Sprachen $L_{1} \text{ und } L_{2}$ somit: $L_{1}\cap L_{2}$ **nicht kontextfrei** sind 

Dank [[Abschluss unter Konkatenation kontextfrei]] sind also auch diese Sprachen kontextfrei:
$L_{1} = \{a^{i}b^{i} | i ≥ 0 \} ◦ \{c^{i} | i ≥ 0 \} = \{a^{i}b^{i}c^{k} | i ≥ 0, k ≥ 0 \}$
$L2 = \{a^{i} | i ≥ 0\} ◦ \{b^{i}c^{i} | i ≥ 0\} = \{a^{i}b^{i}c^{i} | i ≥ 0, k ≥ 0\}$

aber: $L_{1} \cap L_{2}=\{ a^{i}b^{i}c^{i}|i \geq 0 \}$ ist nicht kontextfrei