In der Prädikatenlogic betrachtet man **mehrere Mengen**, statt eine *unendliche Menge an Atomen wie in der Aussagenlogic*
- Menge **V** von Variablen : $x,y,z$
- Menge **C** von Constanten : $a,b,c$
- Menge **P** von  Prädikatensymbole : $p,q,r$
Variablen und Konstante werden auch [[Terme]] genannt 

## Atom
Ein prädikatenlogisches Atom hat die Form $p(t_{1},\dots,t_{n})$ für ein n-Stelliges Prädikatensymbol $p \in P$ und [[Terme]] $t_{1},\dots ,t_{n} \in V \cup C$

>[!Important]
>De Morganesche Gesetze gelten auch im Prädikatenlogic

---

## Konventionen
Hintereinander vorkommende **Quantoren gleicher Art werden zusammengefasst,**
wobei man die Variablen als Liste angibt
*Beispiel:*
- Wir schreiben $∀x, x′.∃y, y′.(p(x, x′) → p(y, y′))$ statt $∀x.∀x′.∃y.∃y′.(p(x, x′) → p(y, y′))$
Negation und Quantifikation „**binden stärker**“ als binäre Junktoren
*Beispiel:*
- Wir schreiben $¬p ∨ q$ statt $(¬p) ∨ q$
- und $∀x.p(x) ∨ q(x)$ statt $(∀x.p(x)) ∨ q(x)$

---
