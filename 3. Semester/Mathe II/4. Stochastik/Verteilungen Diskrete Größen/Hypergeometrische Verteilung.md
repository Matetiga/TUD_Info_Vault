## Definition 
Die **Hypergeometrische Verteilung** beschreibt die Wahrscheinlichkeit, eine bestimmte Anzahl von Erfolgen zu ziehen, **ohne Zurücklegen** aus einer endlichen Population.

- $\textbf{\textcolor{yellow}{Unterschied}}$ mit [[Binomialverteilung]]: Hypergeometrsische Verteilung ist **ohne Zuücklegen**

![[Pasted image 20250128113605.png]]

## Bemerkung  
Die Erwartungswerte der hypergeometrischen Verteilung und der [[Binomialverteilung]] stimmen überein, wenn man $p = \frac{M}{N}$ setzt.  

Die Varianz der hypergeometrischen Verteilung ist für $n > 1$ um den Faktor $\frac{N - n}{N - 1}$ kleiner als die Varianz der Binomialverteilung.  
Der Unterschied nimmt mit wachsendem Stichprobenumfang zu (*Entnehmen ohne Zurücklegen*).  

Für $N \to \infty$ geht die Varianz der hypergeometrischen Verteilung in die Varianz der Binomialverteilung über.  

---


## Grenzwertsatz
$$
\lim_{
\substack{
N \to \infty \\
M \to \infty \\
\frac{M}{N} = p \text{ const.}
}
} 
\frac{\binom{M}{i} \binom{N-M}{n-i}}{\binom{N}{n}}
= \binom{n}{i} p^i (1 - p)^{n-i}
$$
