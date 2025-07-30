## Entscheidbarkeit 
- [[#Entscheidbare Sprachen]]
Eine Sprache L heißt genau dann **entscheidbar** (berechenbar, rekursiv), wenn es eine
TM $M$ gibt, die ihr Wortproblem entscheidet, d.h. $M$ ist Entscheider und $L = L(M)$.
Andernfalls heißt L unentscheidbar.

## Semi-Entscheidbar
- [[#Semi-Entscheibare Sprachen]]
L heißt genau dann $semi-entscheidbar$ (Turing-erkennbar, rekursiv aufzählbar), wenn
es eine TM $M$ mit $L = L(M)$ gibt (auch wenn $M$ kein Entscheider ist)

---

### Entscheidbare Sprachen
Eine Sprache $L$ ist **entscheidbar** (oder rekursiv), wenn es eine Turingmaschine $M$ gibt, die für jede Eingabe $w$ folgende Eigenschaften hat:
- **Falls** $w∈L$, hält $M$ nach endlich vielen Schritten und akzeptiert $w$
- **Falls** $w \not \in L$, hält $M$ nach endlich vielen Schritten und lehnt $w$ ab

Die Turingmaschine $M$ **entscheidet das Wortproblem** der Sprache $L$
- Sie gibt immer ein Ergebnis (*akzeptieren oder ablehnen*) und **bleibt nie in einer Endlosschleife** hängen


### Untenscheidbare Sprachen
Eine Sprache $L$ ist unentscheidbar, wenn es **keine Turingmaschine $\mathcal{M}$** gibt, die für alle Eingaben entscheidet, ob sie zur Sprache gehört oder nicht
Das bedeutet:
- Für manche Wörter $w$ bleibt die Turingmaschine in einer **Endlosschleife** und **gibt keine Entscheidung** aus


### Semi-Entscheibare Sprachen
Eine Sprache $L$ heißt *semi-entscheidbar* (rekursiv aufzählbar oder Turing-erkennbar), wenn es eine Turingmaschine $M$ gibt, die folgendes Verhalten zeigt:
- **Falls** $w∈L$, hält $M$ nach endlich vielen Schritten und akzeptiert $w$
- **Falls** $w∉L$, kann es sein, dass $M$ nie hält (*sie kann in eine Endlosschleife geraten*)

