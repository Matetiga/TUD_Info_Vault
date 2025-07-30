## Definiton
Die Folgerung $P \models F$ kann man als eien endlichen Baum darstellen 
- Jeder Knoten ist ein variablenfreies Atom.
- Jeder Elternknoten entsteht durch Anwendung einer Regel aus $P$ auf seine Kindknoten
- Jeder Blattknoten ist ein gegebener Fakt aus $P$
- Jeder Knoten wird zusätzlich mit der Regel und Substitution $\theta$ bescrhiftet, die zur Ableitung genutzt würde

>[!Important]
>Für jeden Fakt $F \in T_{P}^{\infty}$ gibt es mindestens einen Ableitungsbaum mit Wurzel $P$
### Komplexität
- $P \models F$ ist **EXP-Time vollständig** 

## Beispiel 
![[Pasted image 20250707130144.png]]
