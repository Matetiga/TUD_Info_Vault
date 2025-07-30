## Komplementärsprache 
Sei $L$ eine Sprache, dann ist $\overline{L}$ die Komplementärsprache

---
### Satz
Für jede Sprache $L$ gibt es [[Turing Reduktionen]] $\overline{L} ≤_{T} L$  und $L ≤_{T} \overline{L}$
=> $L$ ist genau [[(Un)Entscheidbarkeit#Entscheidbarkeit|entscheidbar]] wenn $\overline{L}$ [[(Un)Entscheidbarkeit#Untenscheidbare Sprachen|unentscheidbar]] ist

---

## Zwei Halbe Entscheidbarkeit 
### Satz
$L$ ist genau dann **entscheidbar**, wenn $L$ und $\overline{L}$ semi-entscheibar sind

---
## Co-Semi-Entscheidbarkeit 
Ein Problem ist *co-semi-entscheidbar*, wenn sein Komplement *semi-entscheidbar* ist 
- Wenn ein Problem **nur semi-entscheidbar** oder **nur co-semi-entscheidbar** ist, dann ist es **unentscheibar** 
- Co-semi entscheidbare Probleme können auf [[Turing Reduktionen]] reduziert werden