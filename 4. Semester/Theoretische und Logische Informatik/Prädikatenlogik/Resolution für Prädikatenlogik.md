## Algorithmus
1. Logische Formel auf Unerfüllbarkeit reduzieren 
2. Formeln in Klauselnform umwandeln
	- [[Bereinigte Formeln|Formel bereinigen]]
	- [[4. Semester/Theoretische und Logische Informatik/Prädikatenlogik/mit Funktionssymbole/Negationsnormalform|Negationsnormalform]] bilden
	- [[Pränexform]] bilden
	- [[Skolems Funktionen|Skolemform]] bilden
	- [[Konjunktive NormalForm]] bilden
3. Resolutionsverfahren anwenden
	- [[Unifikator|Unifikation]] zum finden passende Klauseln
	-  Bilden von Resolventen bis Terminierung 

### Resolutionsverfahren
1. Umformung in Klauselform 
2. Durchführung von Resolutionsschritten, bei denen jeweils *zwei Klauseln kombiniert werden*
3. Terminierung wenn die leere Klausel auftritt oder keine neuen Klauseln mehr entstehen
- Die Umformung in Klauselform muss jetzt *Quantoren* berücksichtigen.
- Die Resolutionsschritte müssen die *kompliziertere Form von Atomen* (Prädikate mit Termen als Parameter) berücksichtigen.
- Es wird im Allgemeinen möglich sein, unendlich viele Klauseln abzuleiten, ohne jemals die leere Klausel zu erzeugen – *Terminierung ist nicht garantiert*	

### Resolutionssatz
Sei $F$ eine prädikatenlogische Formel und $K_{i} \ (i ≥ 0)$ die vom Resolutionsalgorithmus ermittelten Klauselmengen. Dann sind die folgenden Aussagen äquivalent
- $F$ ist unerfüllbar $\Leftrightarrow$ Es gibt ein $l\geq 0$ mit $\perp \in K_{l}$
### Beispiel
![[Pasted image 20250629122656.png]]