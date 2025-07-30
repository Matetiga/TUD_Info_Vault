Die Menge reguläre Ausdrücke über einem Alphabet $\Sigma$ ist induktiv$^{a}$ wie folgt definiert: 
- $\emptyset$ ist ein  reguläre Ausdrück
- $\epsilon$ ist ein  reguläre Ausdrück
- für jedes  $a \in \Sigma$ ist $a$ ist ein  reguläre Ausdrück

### Semantik  reguläre Ausdrücke
 - $L(\emptyset)=\emptyset$
 -  $L(\epsilon)=\{ \epsilon \}$
 -  $L(a)=\{ a \}  \ \forall a \in \Sigma$
 -  $L((\alpha\beta))=L(\alpha) \circ L(\beta)$
 - $L((\alpha | \beta))=L(\alpha) \cup L(\beta)$
 - $L((\alpha)^{*})=L(\alpha)^{*}$

---