Eine Formel ist genau dann in Pränexform, wenn alle **ihre Quantoren am Anfang** (und ihre Variablen) stehen
Also es hat folgende Form:
$Q_{1}x,\dots,Q_{n}x_{n}.F$
- und Q ein Quantor 

## Umwandlung in Pränexform 
Sei F eine bereinigte Formel in [[4. Semester/Theoretische und Logische Informatik/Prädikatenlogik/mit Funktionssymbole/Negationsnormalform|Negationsnormalform]] . Eine zu F semantisch äquivalente Formel in Pränexform entsteht durch erschöpfende Ersetzung von Teilformeln nach folgendem
Schema:
- $(Qx.G ◦H)  \mapsto Qx.(G ◦H)$
- $(G ◦ Q x.H) \mapsto Qx.(G \circ H)$
für beliebige $Q ∈\{∃, ∀ \}$und$◦∈\{ ∨, ∧ \}$.

### Schritte
1. $\leftrightarrow$ und $\to$ auflösen
2. $\neg$ (Negation) nach innen ziehen ([[4. Semester/Theoretische und Logische Informatik/Prädikatenlogik/mit Funktionssymbole/Negationsnormalform|Negationsnormalform]])
3. Variable umbenennen ([[Bereinigte Formeln]])
4. Quantifikatoren nach vorne ziehen