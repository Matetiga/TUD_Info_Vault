## NP-Vollständig 
wenn sie [[NP-Schwer]] ist und in [[NP]] liegt.

### Beweis Mehtode
Um zu zeigen das ein Problem $L$ NP-vollständig ist :
- Zeige, dass $L \in NP$
- finde bereits eine bekannte NP-schwer Problem $Q$, sodass gilt :
	- $Q \leq_{p} L$ (*Q ist nicht schwieriger als L*)
	- Somit L NP-Schwer und in NP
### Beispiele
-  SAT (NP-Vollständig)
- **Clique** : (Eine Clique ist ein Graph, bei dem jeder Knoten mit jedem anderen direkt durch eine Kante verbunden ist)
- **Unabhängige Menge** :  ( es lässt sich *mit einer Clique* beweisen, da wenn es eine Clique mit $k$ Knoten, dann hat diese Clique ein **Komplementäres** Graph mit $k$ *unabhängige Knoten*)

>[!Important]
>Für $L_{1}$ NP-Vollständig. In welcher Klasse liegt $L_{2}$, wenn :
>$L_{1} \leq_{p} L_{2}$
>- $L_{2}$ ist mindestens so schwer wie $L_{1}$, also es ist **garantiert**, dass $L_{2}$ **NP-Schwer** ist, aber **nicht**, dass $L_{2}$ in **NP liegt**
>
>Für $L_{2}$ NP-Vollständig. In welcher Klasse liegt $L_{1}$, wenn :
>$L_{1} \leq_{p} L_{2}$
>- $L_{1}$ ist nicht schwieriger als $L_{2}$, also **garantiert**, dass $L_{1}$ in **NP** liegt, aber **nicht garantiert**, dass $L_{1}$ **NP-Schwer** ist 

