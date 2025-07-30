
## Definition 
Der Konsequenzoperator $T_{P}$ für ein [[Datalog Regel|Datalog Programm]] P bildet endliche Mengen $F_{I}$
von Fakten auf Mengen von Fakten ab

$$
T_{P}(F_{I})=\{ H\theta \leftarrow B_{1} \land \dots \land B_{n} \in P \text{ und es gibt Substitution } \theta \text{ mit } B_{1}\boldsymbol{\theta}, \dots,B_{n}\theta \in F_{_{I}} \}
$$

### Wichtig
- $T_{P}^{1}=T_{P}= \emptyset$ ist die **Menge aller Fakten** 
- $T_{P}^{i+1}=T_{P}(T_{P}^{i})$ für alle $i \geq 0$
- $T_{P}$ erreicht also nach endlich vielen Schritten einen Grenzwert:
	- $$T_{P}^{\infty}=\bigcup_{i \geq 0} T^{i}_{P}$$
- $T_{P}^{\infty}$ ist das kleinste [[Herbrand Model]]
	- Für einen beliebigen Fakt F gilt:
	- $F \in T_{P}^{\infty}$ gdw. F in jedem Herbrand-Modell vorkommt $\Leftrightarrow P  \models F$
## Beispiel
![[Pasted image 20250707114812.png]]

