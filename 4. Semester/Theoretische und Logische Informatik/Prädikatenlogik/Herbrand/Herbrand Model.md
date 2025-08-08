Die Menge aller *atomare Formeln* 
- also Prädikate ohne Quantoren 
- oder logische Verknüpfungen

>[!Important]
>Ein Herbrand Modell $I$ ist eine Menge, wo Prädikate Elementen aus dem [[Herbrand Universum]] enthalten und die **Formel erfüllen**
>- Es ist eine [[Herbrand Interpretationen| Herbrand Interpretation]], die die gegebene Formel erfüllt 
>- Ist eine Teilmenge der [[Herbrand Basis]]

## Beispiel 
Für die Formel : $G=\forall x,y.(p(a,f(a,x,y)) \lor q(b))$
ist ein mögliches Herbrand Modell, das folgendes:
- Da es eine Logische Oder Operation ist, kann man definieren, dass $q(b)$ **wahr ist**
- Dafür folgt ein Herbrand Modell : 
	- $q^{I_{G}}=\{ b \}$
	- $p^{I_{G}}=\emptyset$
>[!Important]
>Es gibt viele Herbrand-Interpretationen mit denen die Formel erfüllt wird
>Also sie viele mögliche Herbrand Modelle 
>- Aber nicht jede Formel hat ein Herbrand Modell, *da jede Formel nicht erfüllbar ist*
>- z.B $\forall x.(p(x) \land \neg p(x))$

### Unterschied mit [[Herbrand Expansion]]
- Herbrand Modell beschäftigt sich nicht mit der gesamten Formel (nur Prädikate als Einseln)
 - Herbrand Modell, nutzt Elemente aus dem Herbrand Expansion (aber nicht alle Elemente erfüllen die Formel)