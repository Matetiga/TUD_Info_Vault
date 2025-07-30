Die Verteilungsfunktion $F_{\mathcal{X}}$ liefert Information über die Zufallsgröße $\mathcal{X}$, ohne Einselnwahrscheinlichkeiten explizit anzugeben 

### Verteilungsfunktion
Die Verteilungsfunktion von $X$ ist eine Treppenfunktion :

$$
F_X(x) = p(X < x) = 
\begin{cases} 
0, & x \leq x_1 \\ 
p_1, & x_1 < x \leq x_2 \\ 
p_1 + p_2, & x_2 < x \leq x_3 \\ 
\vdots 
\end{cases}
$$

## Definition
Sei $(\Omega, \mathcal{E}, p)$ ein Wahrscheinlichkeitsraum und $\mathcal{X}$ eine [[Zufallsgröße]] 
Die Abbildung: 
mit: 
- $F_{\mathcal{X}}(x):= p(\mathcal{X}<x)$
$$
F_{\mathcal{X}} : \mathbb{R} \to [0,1] : x \mapsto F_{\mathcal{X}}(x)
$$


---
#### Bemerkungen
1. $p(\mathcal{X}<c)=F_{\mathcal{X}}(c)$
2. $p(\mathcal{X}\geq c)=1-F_{\mathcal{X}}(c)$
3. $p(\mathcal{X}=c)=F_{\mathcal{X}}(c+0)-F_{\mathcal{X}}(c)$
4. $p(a<\mathcal{X}<b)=F_{\mathcal{X}}(b)-F_{\mathcal{X}}(a+0)$
5. $p(a\leq\mathcal{X}<b)=F_{\mathcal{X}}(b)-F_{\mathcal{X}}(a)$
6. $p(a<\mathcal{X}\leq b)=F_{\mathcal{X}}(b+0)-F_{\mathcal{X}}(a+0)$
7. $p(a\leq\mathcal{X}\leq b)=F_{\mathcal{X}}(b+0)-F_{\mathcal{X}}(a)$

 $F_{\mathcal{X}}(c+0):$ **Inkludiert den rechtseitigen Grenzwert an der stelle** *c*
 - [[Diskrete Zufallsgröße#Beispiel]]
