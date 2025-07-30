Jedes Jedes Vorkommen einer Variablen in einer Formel ist entweder **frei** oder **gebunden**

## Freie Variablen 
- In einem [[Prädikatenlogic#Atom|Atom]] sind *alle* Vorkommen von **Variablen frei**
- Die freien Vorkommen in $\neg F$ sind dieselben wie in $F$
- Die freien Vorkommen in $(F ∧ G), (F ∨ G), (F → G)$ und $(F ↔ G)$ sind **alle freien Vorkommen aus F und G**
- Die freien Vorkommen in $∀x.F$ und $∃x.F$ sind *dieselben wie in F*, **ohne die Vorkommen von x in F**

## Gebundene Variablen 
Vorkommen von Variablen sind genau dann *gebunden*, wenn sie im **Bereich eines Quantors** ($\forall, \exists$) **auftauchen**


![[Pasted image 20250526214508.png]]


## Wichtig 
- Formeln **ohne freie Vorkommen** von Variablen *heißen geschlossene Formeln* oder *Sätze*
- Formeln mit **freien Vorkommen** von Variablen heißen *offene Formeln*