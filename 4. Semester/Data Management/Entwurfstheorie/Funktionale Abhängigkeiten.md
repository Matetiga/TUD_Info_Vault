[[Volle - Partielle FD]]
## Schreibweise 
$$
A \to B
$$
- $A → B \Leftrightarrow \forall t_{1},t_{2} \in r(RS) : t_{1}[A] = t_{2}[A] \implies t_{1}[B] = t_{2}[B]$
- B ist funktional abhängig von A
Ein Attribut (oder eine Kombination von Attributen) **bestimmt die Werte eines anderen Attributs** (oder Attributkombination)
## Armstrong Axiome
Zur Berechnung von $F^{+}$ (**Hülle** = Menge von Funktionale Abhängigkeiten) 
- *Transitiv*
- *Reflexiv*
- *Verstärkung* ($\text{ falls } A\to B \text{ dann } A \cup C \to B \cup C$)
- *Vereinigungsregel* (Falls $A→B$ und $A→C$ gilt, dann gilt auch $A→B\cup C$)
- *Dekompositionsregel* (Falls $A→B\cup C$ gilt, dann gilt auch $A→B$ und $A→C$)
- *Pseudotransivität* (Falls $A→B$ und $B\cup C→D$ gilt, dann gilt auch $A\cup C→D$)
- [[Volle - Partielle FD]]
#### Trivial 
eine Funktionale Abhängigkeit heißt *Trivial* falls für $A\to B$ , $B \subseteq A$ gilt 

--- 

## Äquivalenz funktionaler Abhängigkeiten
Zwei Mengen F und G von FDs eines Relationenschemas R sind äquivalent, falls :
- $F^{+}= G^{+}$


