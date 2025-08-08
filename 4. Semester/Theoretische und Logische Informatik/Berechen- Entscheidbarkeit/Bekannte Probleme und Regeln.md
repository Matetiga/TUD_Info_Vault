## Problemen
- $P_{Halt}$ : unentscheidbar 
- $\overline{P}_{Halt}$ : unentscheidbar
- $P_{Halt}$ : [[Halteproblem|semi-entscheidbar]]
- $P_{Halt} \leq_{m} P_{Äquiv}$,,
- $P_{Halt} \leq_{m} \overline{P}_{Äquiv}$
	- aber diese Reduktion bedeutet nicht, dass $P_{Halt}$ *nicht semi-entscheidbar* ist, sondern, dass $P_{Halt}$ **mindestens so schwer als** ${P}_{Äquiv}$ ist und somit ist eine **Reduktion möglich**
 
- $P_{Äquiv} \text{ und } \overline{P}_{Äquiv}$ : nicht semi-entscheidbar 
- **Äquivalenzproblem** von Kontextfreie Sprachen ist **unentscheidbar**
- $\overline{P_{Leer}}$ ist semi-entscheidbar
- **Entscheidungsproblem** ist unentscheidbar 
- [[Postsche Korrespondenzproblem]] ist **unentscheidbar**
#### Definitionen
- [[Probleme Beispiele|Semi-Entscheidbare Probleme]]
- [[Unentscheidbare Probleme]]
- [[Prädikatenlogik Unentscheidbarkeit]]
---
## Bekannte Regeln
### Entscheidbarkeit
- Wenn $P$ **entscheidbar**, dann $\overline{P}$ **auch entscheidbar**
- $L$ ist genau dann **entscheidbar**, wenn $L$ *semi-entscheibar* und $\overline{L}$ *co-semi-entscheibar* ist
- Eine **Sprache** K ist genau, dann **entscheidbar**, wenn ihr **Komplement** $\overline{K}$ **entscheidbar** ist 
- Jede **entscheidbare** Sprache ist **auch semi-entscheidbar**
---
### Unentscheidbarkeit
- Wenn $P$ **unentscheidbar**, dann $\overline{P}$ **auch unentscheidbar** 
	- (Beweis durch Widerpruch)
- Dasselbe gilt für Sprachen auch ($L \text{ unentscheidbar, dann } \overline{L} \text{ auch unentscheidbar}$)
---
### Semi-entscheidbarkeit
- Wenn $P$ semi-entscheidbar und $Q \leq_{m} P \implies Q$ auch semi-entscheidbar  
- Jedes **semi-entscheidbare** Problem kann auf das **Halteproblem** [[Many-One Reduktion]] reduziert werden
##### Komplementierung
 - $P$ semi-entscheidbar $\implies \overline{P}$ [[Komplementierung#Co-Semi-Entscheidbarkeit|co-semi-entscheidbar]]
- $P_{1} \leq P_{2} \implies \overline{P}_{1} \leq \overline{P}_{2}$
- Wenn $P$ *semi-entscheidbar* und $\overline{P}$ *semi-entscheidbar* $\implies P$ [[Komplementierung#Zwei Halbe Entscheidbarkeit|entscheidbar]]
- Wenn $P$ *semi-entscheidbar* und $P$ *co-semi-entscheidbar* $\implies$ entscheidbar
---