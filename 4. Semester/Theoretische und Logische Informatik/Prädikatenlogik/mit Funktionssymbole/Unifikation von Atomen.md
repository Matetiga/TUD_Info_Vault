Ein Unifikator für die Menge  $A=\{ A_{1},\dots A_{n} \}$ prädikatenlogische Atome ist eine [[Substitution]] $\theta$ mit $A_{1}\theta=A_{2}\theta=\dots =A_{n}\theta$
- Eine Menge von Atomen ist nur dann unifizierbar, falls alle [[Prädikatenlogic#Atom|Atome]] denselben Prädikat verwenden
	-  Es gilt ein l-stelliges Prädikatensymbol p
	- $A_{i}= p(t_{i,1},\dots,t_{i,l}) \quad \forall i \in \{ 1,\dots,n \}$ 
- Dann ist σ genau dann ein Unifikator für A, wenn σ Unifikator für das folgende Unifikationsproblem $G_{A}$ ist
	- $G_{A} = \{ t_{i,j} \doteq t_{i+1,j} | 1 \leq i \leq n -1, 1\leq j \leq l\}$
- Insbesondere ist der allgemeinste Unifikator für $G_{A}$ auch der allgemeinste Unifikator für $A$

