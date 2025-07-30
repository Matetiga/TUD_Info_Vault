- Bedeutet: Man kann $q$ mit *Symbol* $w$ ein Endzustand erreichen
![[Screenshot from 2024-11-18 13-37-04.png]]
## Schritte
1) Entferne offensichtliche unnötige Zustände
2) Bestimmung des Gleichungssystem (**eine Gleichung pro Zustand**)
3)  Lösen des LGS durch -> Einsetzen oder [[Regel von Arden]]
4) Gib den Ausdruck für die Sprache des NFA an 
---
## Notation 
Für eine eindliche Menge A $=\{ \alpha_{1},\dots,\alpha_{n} \}$ von regulären Ausdrücken schreibt man $\sum_{\alpha \in A}\alpha$ als Abkürzung für $\alpha_{1}|\dots|\alpha_{n}$

### Automat ohne Rekursion
- *Jedes Zustand* wird als **Startzustand** behandelt 
![[Screenshot from 2024-11-18 13-50-18.png]]

### Automat mit Rekursion 
- bei $\alpha_{A} \equiv a\alpha_{B}$
	- dann alle Wörte, die mit a anfangen und von $\alpha_{B}$ akzeptiert werden
	- dass wird für jedes Zustand gemacht 
![[Screenshot from 2024-11-18 13-52-52.png]]
