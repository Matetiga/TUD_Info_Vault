 
## Unifikationsproblem
Ist eine endliche Menge von Gleichungen der Form:
 $$G= \{ s_{1} \doteq, \dots, s_{n} \doteq t_{n} \}$$

## Unifikator
Ein [[Substitution]] $\sigma$ ist genau ein Unifikator für *Unifikationsproblem* G , wenn : $s_{i}\sigma = t_{i}\sigma \text{ für alle } i \in \{ 1,\dots,n \}$
 - Wenn ein **Unifikationsproblem lösbar** ist (d.h., einen Unifikator hat), dann hat es auch einen [[#Allgemeinste Unifikator]]

### Beispiel 
- Man versucht etwas hinzuzufügen, damit beide Seiten von $\doteq$ gleich sind
![[Pasted image 20250623223532.png]]

---
## Allgemeinste Unifikator 
Ein **allgemeinster Unifikator** für ein *Unifikationsproblem* G ist ein Unifikator $\sigma$ für G, so dass $\sigma \preceq \theta$ ([[Substitution#Allgemeine Substitutionen]]) für alle Unifikatoren $\theta$  für G
-  *Die allgemeinsten Unifikatoren von G sind bis auf Umbenennung von Variablen identisch*

![[Pasted image 20250623224458.png]]
