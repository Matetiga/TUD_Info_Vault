- mit Maximum Likelihood
- mit begrenzter Mindestdistanz


## Fehlerkorrektur (FK)
###### Hinzufügung **reduntanter** Stellen **zur Erkennung eines Fehlers UND** Lokalisierung der **Fehlerpositionen**

- Diese Formeln werden benutzt, wenn sowohl **Fehlerkorrektur als auch Fehlererkennung berücksichtigt werden**

---

$$
\begin{gather}
f_{e}= \left\lfloor  \frac{d_{min}}{2}  \right\rfloor &f_{k}= \left\lfloor \frac{d_{min}-1}{2}   \right\rfloor 
\end{gather}
$$

- $f_{e}$ => Ein Code kann **sicher Fehler erkennen**, wenn es **bis zu** $f_{e}$ Fehler gibt
- $f_{k}$ => Steht für die **Anzahl an Fehler**, die **korregiert** werden kann