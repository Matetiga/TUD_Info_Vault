sei $\epsilon >0$ beliebig, fest gewählt

$$
\begin{gather}
\implies\exists N_{a} \quad \forall n\geq N_{a}:\quad |x_{n}-a|<\epsilon  \quad und \\
\exists N_{b} \quad \forall n\geq N_{b}: \quad |x_{n}-b|<\epsilon
\end{gather}


$$

Sei $N:=max(N_{a},N_{b})$ 
Also wir nehmen <span style="color:#ffff00">die grösste zwischen</span> $N_{a},N_{b}$, damit <span style="color:#ffff00">alle Glieder der Folgen beschränkt</span> sind 

$$
\begin{gather}
\forall n\geq N: \quad |x_{n}-a|<\epsilon\ und\ |x_{n}-b|<\epsilon \\
|a-b| = |a -x_{n}+x_{n}-b|
\end{gather}

$$
Dies wird mit Hilfe der **Dreieksungleichung** gemacht

$$
|(a-x_{n})+(x_{n}-b)|\leq|x_{n}-a|+|x_{b}-b| < 2\epsilon
$$
Jeder Summant der rechten Seite ist kleiner als epsilon

Wenn man $\epsilon= \frac{|a-b|}{3}$ kommt man zu einem <span style="color:#ffff00">Wiederspruch!</span> 