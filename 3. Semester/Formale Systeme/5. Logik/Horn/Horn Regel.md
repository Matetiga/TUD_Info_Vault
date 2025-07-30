## Horn Klausel
Klausel mit **höchstens** ein *nicht-negiertes* Literal
- Muss in [[Konjunktive, Disjunktive Normalform|KNF]] sein
- Die Klauseln müssen als eine Implikation dargestellt werden können
$(\neg q \lor \neg p \lor r)\equiv(q\land p)\implies r$

### Alle Literalen sind negiert
- $(\neg q \lor \neg p \lor \neg r) \equiv (q \land p \land r \land \implies 0 )$

### Genau ein Literal nicht negiert und alle andere negiert
$(\neg q \lor \neg p \lor r)\equiv(q\land p)\implies r$

### Genau ein Literal nicht negiert 
$q \equiv q\implies 1$

---
## Horn Formel
Eine *Horn-Formel* ist eine Formel in [[Konjunktive, Disjunktive Normalform|KNF]], welche *nur Horn-Klauseln* enthält

