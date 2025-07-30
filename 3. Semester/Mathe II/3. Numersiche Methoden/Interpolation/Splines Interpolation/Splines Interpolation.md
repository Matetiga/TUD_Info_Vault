
## Definition:  
Eine **Splinefunktion $s$ vom Grad $k$** (Kurz: Spline) zur Unterteilung  
$x_0 < x_1 < \dots < x_n$ ist eine reelle Funktion :
- $s: [x_0, x_n] \to \mathbb{R}$

mit:  

1. Auf jedem Teilintervall $[x_i, x_{i+1}]$ stimmt $s$ mit einer Polynomfunktion vom Grad $\leq k$ überein.  
2. $s$ ist auf dem Intervall $(x_0, x_n)$ $(k-1)$-mal stetig differenzierbar.  

---

### Bemerkung:  
Für $k = 3$ spricht man von **kubischen Splines**.