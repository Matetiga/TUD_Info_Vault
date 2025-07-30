## Typ 2: kontextfreie Grammatiken
- alle Regeln haben die Form $A \to v$ für eine Variable $A$
- *z.B*: $A \to zz$ **aber nicht** $Az\to zz$


#### $\epsilon-$frei
- es gibt keine Regeln der Form: $A\to \epsilon$
- es gibt eine Regel $S\to \epsilon$ und **alle anderen sind** $A\to v \quad mit \ v \neq \epsilon$ und **S kommt nicht** in $v$ vor
	- dann sind alle $\epsilon-$frei kontextfreie Grammatiken auch kontextsensitive
	- *$\epsilon-$frei kontextfreie Grammatiken ezeugen dieselbe Sprache als kontextsensitive