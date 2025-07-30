## Beispiel 
$p(a,x)$
- mit $a \in C$
- mit $x \in V$
	- **für p folgt**: Prädikatssymbole stehen für Relationen gleicher Stelligkeit
	- **für a folgt** : Konstanten stehen für Elemente, die in Relationen stehen können.
	- **für x folgt** : Variablen stehen auch für Elemente, aber ihre verschiedenen Vorkommen können für verschiedene Elemente stehen

Ein Atom $p(a, x)$ ist also wahr, wenn zwischen dem Element, für das $a$ steht, und dem
Element, für das $x$ steht, die Relation besteht, für die $p$ steht

## Interpretieren
Sei $I$ eine Interpretation und $Z$ eine Zuweisung auf $I$: 
- Für eine Variable $x$ definiert man : $x^{I,Z} = Z(x)$ (also den *Wert der Zuweisung*)
- Für eine Konstante $c$ definiert man : $c^{I,Z} = c^{I}$
Für ein Atom $p(t_{1},\dots,t_{n})$ setzen wir so dann: 
- $p(t_{1},\dots,t_{n})^{I,Z}=1$ wenn $\langle t_{1}^{I,Z},\dots , t_{n}^{I,Z}\rangle \in p^{I}$
- $p(t_{1},\dots,t_{n})^{I,Z}=0$ wenn $\langle t_{1}^{I,Z},\dots , t_{n}^{I,Z}\rangle \not \in p^{I}$

> [!Important]
> Wir verwenden Interpretationen und Zuweisungen auf zwei Ebenen, die man nicht verwechseln sollte
> 1. um Terme $t$ auf Elemente $t^{I,Z} ∈ \Delta I$ abzubilden
> 2. um Atome $A$ auf Wahrheitswerte $A^{I,Z} ∈ \{0, 1 \}$ abzubilden.






