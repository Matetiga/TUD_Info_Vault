## Kriterien 
1. Eine Zerlegung des Schemas RS in RS1 und RS2 hat keinen Informationsverlust, wenn für jede mögliche (gültige) Ausprägung R in RS gilt:
$$
R=\pi_{R_{1}}(R) \Join \pi_{R_{2}}(R)
$$
- also die Rekonstruktion aus der **zerlegten Tabellen muss genauso** wie die *(originalle) Tabelle* sein

![[Pasted image 20250603154417.png]]

2. Wenn man die andere tabellen mit einander schneiden dann muss einer Funktionale Abhängigkeit (Schlüssel) rauskommen, mit dem einer der zwei Tabellen komplett erreichen können
	- $R_{1} \cap R_{2}=R_{1} \lor R_{1} \cap R_{2}=R_{2}$
	- für $R_{1} \text{ mit } : B\to A$
	- für $R_{2} \text{ mit } : B\to C$
	- dann folgt bei dem Schnitt $B \to \{ BA \} \text{ oder } \{ BC \}$ und somit entweder die Tabelle $R_{1} \text{ oder } R_{2}$



