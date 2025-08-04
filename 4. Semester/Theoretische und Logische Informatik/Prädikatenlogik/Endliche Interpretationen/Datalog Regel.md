## Definition 
Eine Formel der Form:
$$\forall x_{1},\dots,x_{l}.((B_{1} \land\dots \land B_{n}) \to H)$$
- H heißt **Kopf**
- $(B_{1} \land\dots \land B_{n})$ heißt **Rumpf** ($n \in \mathbb{N}$)
	- *Jede Variable muss im Kopf und Rumpf vorkommen*
- Ein **Fakt** ist eine variablenfreien Regel mit $n=0$
- **Alle Variablen sind Allquantifiziert** (also syntaktische Varianten [[Skolems Funktionen|skolemisierte Klauseln]])
- Ein **Datalog Programm** ist eine Menge von Datalog-Regeln (einschl. Fakten).


### Satz
Für ein Datalog-Programm P ist $T^{\infty}_{P}$ das kleinste [[Herbrand Model]]
Das heißt: Für einen *beliebigen Fakt F* gilt

$$
F \in T^{\infty}_{P} \Leftrightarrow \text{ F in jedem Herbrand-Modell vorkommt } \Leftrightarrow P \models F
$$