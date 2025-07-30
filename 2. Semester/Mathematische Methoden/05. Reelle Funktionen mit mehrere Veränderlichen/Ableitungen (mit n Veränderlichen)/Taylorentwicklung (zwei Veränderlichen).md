### Taylor Polynome mit zwei Variablen
[[Taylor Polynome]]

---
#### Gegeben
$z=f(x,y)$ in der Umgebung $(x_{0},y_{0})$, $(n+1)$ -mal stetig differenzierbar


### Dann gilt:
mit => $h=(x-x_{0})$ und $k=(y-y_{0})$
$$
\phi(t)=f(x_{0}+t\cdot h, y_{0}+t\cdot k)
$$
## $\implies$ Taylorentwicklung von $\phi$ an der Stelle $=0$
$$
\phi(t)=\phi(0)+\phi'(0)\cdot t+ \frac{1}{2!}\phi''(0)\cdot t^{2}+\dots+ \frac{1}{n!}p^{(n)}(0)\cdot t^{(n)}+R(t,0)
$$
=> Ableitungen von $\phi^{(i)}(t)$ bestimmt man mit der [Kettenregel](obsidian://open?vault=TU-Vault&file=2.%20Semester%2FMathematische%20Methoden%2F05.%20Reelle%20Funktionen%20mit%20mehrere%20Ver%C3%A4nderlichen%2FAbleitungen%20(mit%20n%20Ver%C3%A4nderlichen)%2FAbleitungsregeln)


$$
\phi'(t)=1\cdot f_{x}\cdot h+1\cdot f_{y}\cdot k
$$
$$
\phi''(t)=1\cdot f_{xx}\cdot h^{2}+2\cdot f_{xy}\cdot h\cdot k+1\cdot f_{yy}*k^{2}
$$
- Analogie zur Binomischen Formel 

		1
	 1      1	
	1      2      1
  1    3      3    1
       ...
---
