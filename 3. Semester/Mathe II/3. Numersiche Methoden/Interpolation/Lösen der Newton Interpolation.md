Vorteil über den anderen ist, dass beim Newton Form kann man neue Stellen hinzufügen ohne das ganze wieder bestimmen zu müssen 

##### Newton Polynome aufstellen: 
- $N_{0}(x),N_{1}(x),\dots,N_{n}(x)$
- [[Newton Interpolation]]

---
## Ansatz
- $p(x)=c_{0}\cdot N_{0}(x)+c_{1}\cdot N_{1}(x)+\dots+c_{n}\cdot N_{n}(x)$
- Ermittlung von $c_{0},c_{1},\dots,c_{n}$ mit [[Steigungspiegel]]

#### Ergebnis
- Newton Interpolationspolynom der Orndung *n* 
$$
p(x)=\sum^{n}_{k=0} c_{k}\cdot N_{k}(x)
$$

##### Bemerkung:
- $p_{n+1}(x)=p(x)+c_{n+1}\cdot N_{n+1}(x)$
---
### Beispiel
![[Screenshot from 2024-12-16 17-17-44.png]]![[Screenshot from 2024-12-16 17-23-38.png]]