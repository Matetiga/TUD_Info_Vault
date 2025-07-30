Automat, das kein unendliches Speicher hat
- bleibt stehen am letzten Bandstelle
- sind [[Nichtdeterministische TM]]
- Das **Band** hat eine feste Länge, die höchstens proportional zur Eingabegröße ist.
## Übergangsrelation 
Die Definition der **Übergangsrelation** $\vdash$ für TMs wird für LBAs also wie folgt geändert:  

Sei $wqav$ eine Konfiguration, mit $w, v \in \Gamma^*$, $a \in \Gamma$ und $q \in Q$;  
sei $\delta(q, a) = \langle r, b, R \rangle$.  

- Falls $v \neq \epsilon$, dann $wqav \vdash wbrv$ (wie zuvor);  
- Falls $v = \epsilon$, dann $wqav \vdash wrb$ (neu).
