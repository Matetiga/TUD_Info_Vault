
## Definition
Mit dem [[Herbrand Universum]] als [[Interpretationen#Domäne|Domän]] kann man Interpretationen definieren, die
Terme „durch sich selbst“ interpretieren:

Eine Herbrand-Interpretation für eine Formel F ist eine Interpretation I, für die gilt:
- $\Delta^{I}=\Delta_{F}$ ist das [[Herbrand Universum]] von F
- für jeden [[Terme|Term]] gilt $t \in \Delta_{F}$ gilt $t^{I}=t$
Ist genau ein [[Herbrand Model]] für F, wenn $I \models F$ gilt

### Lemma
Für jede *Herbrand Interpretation* $I$, jede *Zuweisung* $Z$ für $I$, jeden Term
$t ∈ ∆I$ und jede Formel $F$ gilt
$$
I,Z\{ x \mapsto t \} \models F \Leftrightarrow I,Z \models F\{ x \mapsto t \}
$$
- Also es ist äquivalent, ob man x in semantische Ebene interpretiert oder ob man x syntaktisch ersetzt

### Beispiel
![[Pasted image 20250629131653.png]]