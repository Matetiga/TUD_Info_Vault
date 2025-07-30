## Definition

Die Herbrand Expansion $HE(F)$ einer Formel $F=\forall x_{1},\dots,x_{n}.G$ in [[Skolems Funktionen|Skolemform]] ist die Menge :
$$HE(F)=\{ G\{ x_{1} \mapsto t_{1},\dots,x_{n} \mapsto t_{n} \}| t_{1},\dots,t_{n} \in \Delta_{F} \}$$

$HE(F)$ ist also die (möglicherweise unendliche) *Menge variablenfreier Sätze*, die in
Herbrand-Modellen von F gelten müssten

>[!Important]
>Ein Satz ist eine Formel in der keine Variablen vorkommen
### Unterschied mit [[Herbrand Model]]
Herbrand Expansion beschäfigt sich mit der gesamten Formel, also *alle Prädikate*, die **mit logische Verknüpfungen zusammen sind** 


---

## Satz von Gödel, Herbrand & Skolem
Eine Formel F in Skolemform ist genau dann erfüllbar, wenn [[Herbrand Expansion|HE(F)]] aussagenlogisch erfüllbar ist

---
## Satz von Herbrand 
Eine Formel F in [[Skolems Funktionen|Skolemform]] ist genau dann unerfüllbar, wenn eine **endliche**
**Teilmenge** von [[Herbrand Expansion|HE(F)]] aussagenlogisch unerfüllbar ist
- *Jede unerfüllbare aussagenlogische Formelmenge hat eine endliche unerfüllbare Teilmenge*

