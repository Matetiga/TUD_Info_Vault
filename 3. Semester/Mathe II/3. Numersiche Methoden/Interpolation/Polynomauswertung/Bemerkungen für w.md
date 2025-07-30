#### Definition:  
Sei $K$ ein Körper, $\omega \in K \setminus \{0\}$.  
$\omega$ heißt eine **$(n+1)$-te Einheitswurzel** in $K$, wenn $\omega^{n+1} = 1$ gilt.

1) $\omega$ ist eine **$(n+1)$-te Einheitswurzel** in $K$ genau dann, wenn $\omega$ eine Nullstelle des Polynoms  
	- $f(x) = x^{n+1} - 1$
  ist.

2) $\omega$ ist eine **$(n+1)$-te Einheitswurzel** in $K$ genau dann, wenn die Ordnung von $\omega$ in der multiplikativen Gruppe von $K$ ein Teiler von $n+1$ ist.

3) Sei $K$ ein Körper, $\omega \in K \setminus \{0\}$.  
	- $\omega$ heißt eine **primitive $(n+1)$-te Einheitswurzel** in $K$, wenn $\omega$ in der multiplikativen Gruppe von $K$ die Ordnung $n+1$ hat.

 4) Für jede primitive $(n+1)$-te Einheitswurzel $\omega$ gilt:  
	- $|\langle \omega \rangle| = \{ \omega^0, \omega^1, \ldots, \omega^n \} = n + 1 \quad \text{mit} \quad \omega^{n+1} = \omega^0$
		- (Im Exponenten kann man modulo $n+1$ rechnen.)

5) Ist $\omega$ eine primitive $(n+1)$-te Einheitswurzel in $K$, dann gilt:  
	- $\omega^j \text{ ist eine primitive } (n+1)\text{-te Einheitswurzel} \quad \Leftrightarrow \quad ggT (j, n+1) = 1$
---

#### Beispiel:  
$\omega$ ist eine primitive $8$-te Einheitswurzel  
$$\Rightarrow \omega^1, \omega^3, \omega^5, \omega^7 \text{ sind primitive $8$-te Einheitswurzeln}$$
---

## Lemma 
Lemma : Ist $w$ eine *primitive (n+ 1) -te Einheitswurzel* im Körper K
dann gilt :
$$
\sum^{n}_{k=0}(w^{\alpha})^{k}=
\begin{cases}
n +1 & \alpha=0\\ 
0&\alpha \in \{ 1,2,\dots,n \}
\end{cases}
$$
