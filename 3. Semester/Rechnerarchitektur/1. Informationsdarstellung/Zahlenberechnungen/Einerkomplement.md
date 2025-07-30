Im Vergleich zu [[3. Semester/Rechnerarchitektur/1. Informationsdarstellung/Zahlenberechnungen/Zweierkomplement]], ist *Einerkomplement schlechter*, da es $0 \text{ und } -0$ gibt, also weniger Platz für Zahlen
## Einerkomplement 1-C
von A mit $n$ Bits ist:
$\tilde{A}(1)=2^{n}-1-|A|$

---
### Beispiel 
mit $n=4$
- 1-C von $A=-6 \Leftrightarrow (6)=2^{4}-1-|A|=16-2-6=9$
- Binärdarstellung von $9\implies 1001_{2}$

### 2. Methode
- mit der Berechnung der Betrag von $-6\implies 0110_{2}$
- Komplementieren der Bits: $1001_{2}$
