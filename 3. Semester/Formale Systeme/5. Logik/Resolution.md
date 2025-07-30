Ein neues Klausel entsteht aus der Vereinigung zweier Klauseln

#### Klausel-Form
- Literalen sind **disjuntkiv** $(\lor)$ verbunden 
- Klauseln sind mit **konjunktiv** $(\land)$ verbunden

## Definition 
- in [[Konjunktive, Disjunktive Normalform|KNF]] 
Gegeben seien zwei Klauseln $K_{1}$ und $K_{2}$ für die es ein Atom $p \in P$ mit $p \in K_{1}$ und $\neg p \in K_{2}$. Die Resolvente von $K_{1}$ und $K_{2}$ bezüglich $p$ ist die **Klausel**:
$$
(K_{1} \backslash \{ p \})\cup(K_{2} \backslash \{ \neg p \})
$$
---

### Beispiel 
Resolventen für die Menge $\{ \{ \neg A, \neg B \},\{ A, B \}, \{ \neg B, \neg C \}, \{  B,  C \}, \{ \neg C, \neg A \}, \{ A,B,C \}, \{ \neg B \}\}$
zum Beispiel:
- $\{ B,\neg A \}$ aus $\{ B,C \} \text{ und  } \{ \neg C, \neg A \}$
	- da $C$ in beide Klauseln (einmal *nicht negiert und einmal negiert* vorkommt) bildet sich das Resolvent $\{ B,\neg A \}$
	- man "**resolviert**" nach $C$
- $\{ A \}$ aus $\{ A,B \} \text{ und } \{ \neg B \}$
- $\{ B, \neg B \}$ aus $\{ B,C \} \text{ und }\{ \neg B, \neg C \}$
