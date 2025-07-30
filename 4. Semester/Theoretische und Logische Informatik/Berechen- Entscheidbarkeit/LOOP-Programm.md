## Eigenschaften
- Es gibt **berechenbare totale Funktionen**, die **nicht LOOP-berechenbar** sind
- Schwacher als eine [[WHILE-Programm]], da es immer terminiert (deswegen auch *nicht Turing Complete*)
- **LOOP-Programme terminieren immer nach endliche viele Schritte**
- Können nicht jede berechenbare Funktion berechnen (Ackermann Funktion, LOOP Busy Beaver)
## Syntax
![[Pasted image 20250414095145.png]]

---
## Funktionsweise 
### Eingabe
- Liste von *k* natürliche Zahlen
### Ausgabe
- Eine natürliche Zahl

---
## Beispiele LOOP-Berechenbare Funktionen 
- Wortproblem : [[Reguläre Sprachen]], [[Kontextfreie Sprachen]], kontextsensitive Sprachen
- Alle Probleme in NP
- alle gängige Algorithmen : (Soriterung, Suchen, Optimieren, ...)

### Berechenbare Funktionen
**Korollar**: Jeder Algorithmus, der in Zeit O($n^{n^{\dots^{x}}}$) – oder weniger – läuft, berechnet eine LOOP-berechenbare Funktion. Insbesondere sind alle polynomiellen, exponentiellen oder mehrfach exponentiellen Algorithmen in LOOP implementierbar
- $n \cdot x$
- $x^{n}$
- $n^{x}$
- $n^{n^{\dots^{x}}}$ 