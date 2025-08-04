-  ist [[(Un)Entscheidbarkeit#Semi-Entscheidbar|semi entscheidbar]]
- und [[(Un)Entscheidbarkeit#Untenscheidbare Sprachen|unentscheidbar]]

## Beweis
Eine Turingmaschine, die das Halteproblem erkennt, ist leicht skizziert:
-  Wenn die Eingabe die Form enc(M)##enc(w) hat
-  dann simuliere M auf Eingabe w.
-  Wenn M hält, dann halte und akzeptiere

Im Wesentlichen ist die TM für das Halteproblem also die [[Turingmaschinen Kodieren#Universelle Turing Maschine|Universelle Turing Maschine]]

---


## Satz
Jedes **semi-entscheidbare** Problem kann auf das **Halteproblem** [[Many-One Reduktion]]
reduziert werden