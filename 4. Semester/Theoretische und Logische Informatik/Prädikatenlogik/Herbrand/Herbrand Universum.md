## Definition
Sei $a$ eine beliebige Konstante. Das *Herbrand-Universum* $∆F$ für eine Formel F ist die
Menge **aller variablenfreien Terme**, die man mit Konstanten und Funktionssymbolen in
F und der zusätzlichen Konstante a bilden kann:
- $a \in \Delta_{F}$
- $c \in \Delta_{F}$ für jede Konstante in F
- $f(t_{1},\dots ,t_{n}) \in \Delta_{F}$ für jedes n-stellige Funktionssymbol aus F und alle Terme $t_{1},\dots ,t_{n} \in \Delta_{F}$

>[!Important]
>Das Herbrand Universum betrachtet **nur die Funktionen und keine Prädikate** 
>Die Elemente aus dem Universum müssen nicht die Konstanten in einer Funktion berücksichtigen (z.B.: für die Formel $f(x,a)$ und a eine Konstante, ist $f(a,f(a))$ Element des Universums )

### Anmerkung 
Das Herbrand-Universum ist **immer abzählbar**, *manchmal endlich* und
**niemals leer**

---
## Herbrand Konstante
Eine Konstante wird im Universum hinzugefügt, nur wenn es keine andere Konstanten hat 
- Somit ist ein Universum niemals leer
- mit $c$ als die **Herbrand Konstante**

## Beispiel
Für die Formel $G=\forall x,y.(p(a,f(a,x,y)) \lor q(b))$
$$
\Delta_{G}=\{ a,b,f(b,c,b),q(f(a,c,b),\dots)\}
$$
- Da man im Universum ist, dürfen Konstanten ersetzt  werden
