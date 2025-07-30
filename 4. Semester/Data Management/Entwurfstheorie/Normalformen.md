## 1. Normalform
- Keine mehrdeutige Attributen
- Eine Relation ist in der ersten Normalform, wenn alle Attribute der Relation *atomar* sind (**Werte können nicht mehr zerlegt werden**)
- Zusammengesetzte und mehrwertige Attribute sind nicht erlaubt
### Beispiel
![[Pasted image 20250602114744.png]]

## 2. Normalform
- Wenn es in 1. Normalform und ...
- Jedes **Atributt** ist entweder **Teil eines Kandidatenschlüssels** 
- *Oder* von jedem **Kandidatenschlüssel** voll [[Funktionale Abhängigkeiten|funktional abhängig ]]
### Beispiel
![[Pasted image 20250602114719.png]]

## 3. Normalform
- Ein Relationenschema ist in der 3. Normalform (3NF), wenn für alle Abhängigkeiten $X \to A$ mit $X \subset R$, $A \in R \text{ und } A \not \in X$ gilt :
	- *X enthält einen Schlüssel von R*, oder *A ist Teil eines Schlüsselkandidaten*
- Keine funktionalen Abhängigkeiten von Nichtschlüsselattributen innerhalb von Relationen
- Die 3. Normalform **beseitigt Abhängigkeiten von Nicht-Schlüsselattributen**
### Beispiel
![[Pasted image 20250602114756.png]]