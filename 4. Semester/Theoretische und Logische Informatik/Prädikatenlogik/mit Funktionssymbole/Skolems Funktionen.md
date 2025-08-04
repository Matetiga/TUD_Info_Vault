Existenz Quantor kann man auch als Auswertung einer Funktion angesehen werden
- Leere Funktionen werden auch als Konstanten betrachtet 

![[IMG_2999.jpeg]]


## Skolemisierung 
*Skolemisierung führt nicht zu semantisch äquivalenten Formeln*
Eine Formel F in [[Pränexform]] ist genau dann erfüllbar, wenn die Skolemisierung
von F erfüllbar ist
- Die Reihenfolgen in dem man die Quantoren ordnet ist wichtig bei Skolemisierung 
- Bei der Skolemisierung ist die **Existenz Quantor, von alle vorherige All-Quantoren abhängig**

### Schritte
1. $\leftrightarrow$ und $\to$ auflösen
2. $\neg$ (Negation) nach innen ziehen ([[4. Semester/Theoretische und Logische Informatik/Prädikatenlogik/mit Funktionssymbole/Negationsnormalform|Negationsnormalform]])
3. Variable umbenennen ([[Bereinigte Formeln]])
4. Quantifikatoren nach vorne ziehen
5. $\exists$ Quantoren duch Funktionen ersetzen (*Leere Funktionen sind auch Konstanten*)

### Beispiele
Für die Formel $∀x.∃y.∀z.∃v.p(x, y, z, v)$ ergibt sich
- Skolemisierung von **y**: $∀x.∀z.∃v.p(x, f (x), z, v)$
- Skolemisierung von **v**: $∀x.∀z.p(x, f (x), z, g(x, z))$


--- 
# Sätze
## Satz mit Herbrand Modell
Ein Satz F in **Skolemform** ist genau dann erfüllbar, wenn F ein [[Herbrand Interpretationen|Herbrand Modell]]
hat

![[Herbrand Expansion#Satz von Gödel, Herbrand & Skolem]]
![[Herbrand Expansion#Satz von Herbrand]]