Diese Probleme können in *polynomielle Zeit* für [[1. deterministische Endliche Automaten DFA]] berechnet werden


**Wortproblem** 
- *Eingabe*: ein FA $M$ und ein Wort w ∈ $Σ^{*}$
- *Ausgabe*: „ja“ wenn $w ∈ L(M)$ und „nein“ wenn $w \not \in L(M)$
- für [[Reguläre Sprachen]] kann in **linearer Zeit** bestimmt werden

**Leerheitsproblem** 
- *Eingabe*: ein FA $M$ über Alphabet $Σ$
- *Ausgabe*  „ja“ wenn $L(M) = ∅$ und „nein“ wenn $L(M) \neq ∅$

**Inklusionsproblem** 
- *Eingabe*: zwei FAs $M_{1}$ und $M_{2}$ über Alphabet $Σ$
- *Ausgabe*: „ja“ wenn $L(M_{1}) ⊆ L(M_{2})$; andernfalls „nein“
- falls [[2. Nichtdeterministische endliche Automaten NFA]] : exponentielle Zeit

**Äquivalenzproblem**
- *Eingabe*: zwei FAs $M_{1}$ und $M_{2}$ über Alphabet $Σ$
- *Ausgabe*: „ja“ wenn $L(M_{1}) = L(M_{2})$; andernfalls „nein“
- falls [[2. Nichtdeterministische endliche Automaten NFA]] : exponentielle Zeit

**Endlichkeitsproblem**
- *Eingabe*: ein FA $M$
- *Ausgabe*: „ja“, wenn $L(M)$ endlich ist; andernfalls „nein“

**Universalitätsproblem**
- *Eingabe*: ein FA $M$
- *Ausgabe*: „ja“, wenn $L(M) = Σ^{*}$; andernfalls „nein“