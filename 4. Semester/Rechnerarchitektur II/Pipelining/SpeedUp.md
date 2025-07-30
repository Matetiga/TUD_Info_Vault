- $S_{p}$ SpeedUp
- $T_{1}$ Zeitschritte Sequentiell
- $T_{p}$ Zeitschritte Parallel
- $n$ Anzahl der Befehle
- $p$ Anzahl der Pipeline-Segmente

## Einlaufsphase 
Phase mit höchstens viele Parallelität 


- Für ein Prozess gilt: $T = k \cdot t_{s}$
- Für n Prozesse gilt: $T_{seq}= n \cdot k \cdot t_{s}$
- Für die PipeLine verarbeitung : $T_{pip}=(k-1) \cdot t_{s}  +n \cdot t_{s}=(k-1+n) \cdot t_{s}$

$$
S_{p}=\frac{T_{seq}}{T_{pip}}= \frac{n\cdot k}{(k-1+n)}
$$
- Falls $n=1 \implies S_{P}=1$ also Pipeline-Rechner funktioniert wie *Sequenzieller Rechner*
- Falls $n > > k \implies S_{p} \approx k$ , je größer die Segmentierung, desto *höher der Geschwindigkeitsgewinn*


--- 
## SpeedUp durch Chaining
$S_{p}=\frac{T_{p} \text{ ohne Chaining}}{T_{p} \text{ mit Chaining}}$

$$
S_{p}=\frac{k_{1}-1+n + k_{2}-1+n}{(k_{1}+k_{2})-1+n}
$$

- für $n \to \infty \implies S_{p}=2$