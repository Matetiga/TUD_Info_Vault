- [[Normalformen#3. Normalform| 3. NormalForm]]
## Generierung 
1. Bestimme die [[Kanonische Überdeckung]] $F_{c}$ der Menge $F$
2. Konstruiere eine Relationsschema aus der einselne Funktionale Abhängigkeiten aus $F_{c}$
3. Führe Schritt 2. solange man einen Schlüsselkandidat erzeugt
	- so erzeuge zusätzlich eine Relation mit dem Schema $R_{K} = K$ und $F_{K} = \emptyset$, wobei K ein Schlüsselkandidat von R is
4. Eliminiere dei Schemata $R_{A}$ die in einem anderen Schema enthalten sind


### Beispiel 
![[Pasted image 20250602151449.png]]


## Boyce/Codd-Normalform
Anders als  [[Normalformen#3. Normalform| 3. NormalForm]] ist X bei Boyce/Codd-Normalform das einzige was einen Schlüssel von R enthält 
- Die Boyce/Codd-Normalform beseitigt Abhängigkeiten unter Attributen, die Teil eines Schlüsselkandidaten sind, d.h. jede Determinante ist ein Schlüsselkandidat
### Erzeugung 
- Zerlegung von R in $R_{1}$ und $R_{2}$
- Erstelle eine Liste aller Determinanten, aus den nicht BCNF-gültigen Abhängigkeiten
- Für jede Determinante, die kein Schlüsselkandidat ist, erstelle eine neue Relation $R_{1}$ aus der funktionalen Abhängigkeit ($X→ \{A \} \text{ wird zu  }R_{1}:= X \cup \{A \}$ )
- Erhalte nur die Determinante in der Originalrelation! ($R_{2} := R – \{A \}$)
### Beispiel
![[Pasted image 20250602153507.png]]