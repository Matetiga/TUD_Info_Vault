Die Menge aller *atomare Formeln* 
- also Prädikate ohne Quantoren 
- oder logische Verknüpfungen

## Beispiel
- Formel: $\forall x \exists y P(x, y)$
- [[Skolems Funktionen#Skolemisierung|Skolemisierung]]: $\forall x P(x, f(x))$ 
- [[Herbrand Universum]]: $\{a, f(a), f(f(a)), \dots\}$
- **Herbrand Model**:$\{P(a, f(a)), P(a, f(f(a))), P(f(a), f(f(a))), \dots\}$(alle möglichen atomaren Instanzen des Prädikats $P(x, y)$

### Unterschied mit [[Herbrand Expansion]]
- Herbrand Modell beschäftigt sich nicht mit der gesamten Formel (nur Prädikate als Einseln)
- also ohne logische Verküpfungen