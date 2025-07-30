## Definition 
Sei $p(x) := a_n x^n + \dots + a_1 x + a_0 \in K[x] \ (\text{K Körper}), \ \hat{k} \in K$.  
Man nennt:  
- $p(k) := a_n {k}^n + \dots + a_1 {k} + a_0$
die **Auswertung von $p(x)$ an der Stelle ${k}$**.  

Die **Polynomfunktion** zu $p(x)$ ist die Abbildung:   
- $K \to K : \hat{k} \mapsto p(\hat{k})$

---

## Bemerkung  
Zur Auswertung von $p(x) = a_n x^n + \dots + a_1 x + a_0$ in der Form  : 
- $p(x) = a_0 + x \cdot (a_1 + x \cdot (a_2 + \dots + x \cdot (a_{n-1} + x \cdot a_n)))$
- ([[Horner Schema]])
benötigt man $n$ Multiplikationen und $n$ Additionen.
