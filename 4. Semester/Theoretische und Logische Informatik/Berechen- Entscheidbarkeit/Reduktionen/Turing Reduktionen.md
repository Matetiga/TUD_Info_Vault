## Definition 
Ein Problem $P$ ist genau dann Turing-reduzierbar **auf ein Problem** $Q$ 
(in Symbolen: $P ≤_{T} Q$), wenn man $P$ mit Hilfe eines *Orakels* für Problem Q in polynomielle Zeit lösen kann.
- Ein **Orakel** für Q liefert sofort die Antwort auf jede Instanz von Q
- *Turing-Reduktion bedeutet*, dass man Problem $P$ lösen kann, wenn man die Fähigkeit hat, Problem $Q$ beliebig oft zu lösen.

### Beispiel
![[Pasted image 20250417103132.png]]

Nehmen wir an, wir haben zwei Probleme:

- **Problem A**: Entscheiden, ob eine Turing-Maschine M auf einer Eingabe w anhält (das Halteproblem).
- **Problem B**: Entscheiden, ob eine Turing-Maschine M auf einer Eingabe w eine bestimmte Ausgabe produziert.

Um zu zeigen, dass $A≤_TB$, könnten wir eine Turing-Maschine konstruieren, die A löst, indem sie das Orakel für B verwendet:

1. Die Turing-Maschine $M_{A}$​ mit Orakel für B simuliert M auf w.
2. Sie fragt das Orakel für B , ob M auf w eine bestimmte Ausgabe produziert, die nur bei einem Halt der Maschine möglich ist.
3. Basierend auf der Antwort des Orakels entscheidet $M_{A}$​, ob M auf w anhält.

In diesem Fall ist das Halteproblem Turing-reduzierbar auf das Problem der Ausgabebestimmung, da wir A mit Hilfe von B lösen können

---
## Andere Reduktionsmethode : [[Many-One Reduktion]]
![[Many-One Reduktion#Vergleich mit Turing Reduktionen]]


---

## Un/Entscheidbarkeit zeigen
Mit Turing-Reduktionen können wir **Entscheidbarkeit oder Unentscheidbarkeit** zeigen, aber *nicht Semi-Entscheidbarkeit*


---

