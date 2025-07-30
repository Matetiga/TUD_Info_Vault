## Satz 
ein [[Endliche Körper GF]] mit $q$ Elementen enthält eine *primitive **n**-te Einheitswurzel* genau dann, wenn: 
- $n |q-1$
- Allgemein gilt: $n|q^{k}-1 \Leftrightarrow q^{k} \equiv 1 (\text{ mod }n)$
	- mit: $k=\text{ord}_{n}(p)$ ist das kleinste $k \in \mathbb{N} \backslash \{ 0 \}$
		- $ord_{n}(p)$ = Ordnung von $p$ in der [[Einheitengruppe]] $\mathbb{Z}^{*};\cdot$ mit $\mathbb{Z}_{n}=\{ x \in \mathbb{Z}_{n}| \text{ggt}(x,n)=1 \}$
		- [[#Beispiel]]
---
## Existenz einer primitiven n-te Einheitswurzel 
Sei $\alpha$ ein primitives **n**-te Einheitswuzel in $GF(q^{t})$
$$
\alpha \text{ exist.} \Leftrightarrow n|p^{t}-1
$$
#### Anzahl der n-ten primitiven Einheitswurzel
- und $n$ teilt $p^{t}-1$
$\phi(n)$

---
## primitiven n-ten Einheitswurzel
- primitiven n-ten Einheitswurzel **erzeugen alle [[n-ten Einheitswurzel]] durch potenzieren**
$\alpha$ heißt *primitiven n-te Einheitswurzel* in GF(q) , wenn $|\langle \alpha \rangle| = n$ gilt 
- mit: 
	- $|\langle \alpha \rangle|=\{ \alpha^{0}, \alpha^{1}, \dots, \alpha^{n-1} \}$
	- und : $\alpha^{0}=\alpha^{n}$
![[Screenshot from 2024-12-02 19-11-41.png]]

---
#### Beispiel 
Gesucht ist das kleinste $k> 0$, so dass endliche Körper $GF(2^{k})$ eine primitive **15-te Einheitswurzel** enthalten
$$
\begin{gather}
15|2^{k}-1 \Leftrightarrow 2^{k}-1 \equiv 0 (\text{ mod }15)\\
\Leftrightarrow 2^{k} \equiv 1\\
\text{ mit : } k=4
\end{gather}
$$![[Screenshot from 2024-12-02 19-33-42.png]]