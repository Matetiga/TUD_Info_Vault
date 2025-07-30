Beste Methode zur Beschreibung der Sprachen 
- **Ersetzungsregeln um Wörter zu erzeugen**
- zwei unterschiedliche Grammatiken können dieselbe Sprache beschreiben


---

## Eigenschaften
Grammatik $G$ ist ein 4-Tupel: $G=\langle V, \Sigma, P, S \rangle$
- $V$ : ist eine Menge von **Variablennamen**
- $\Sigma$ : ist das **Alphabet**, *disjunkt* zu $V$ (also: $\Sigma \cap V=\emptyset$)
- $P$ : Menge von **Produktionsregeln** der From: $w\to v$ für beliebige Wörter $w$ und $v$ über $\Sigma \cap V$ mit $w,v \in (\Sigma \cap V)^{*}$ und $w \not \in \Sigma^{*}$
- $S$ : **Startvariable** aus $V$

