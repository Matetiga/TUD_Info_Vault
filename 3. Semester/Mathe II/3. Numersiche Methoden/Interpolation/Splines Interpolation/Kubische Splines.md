### Gegeben:
- **Unterteilung:** $x_0 < x_1 < \dots < x_n$  
- **Interpolationsbedingungen:** $(x_0, y_0), (x_1, y_1), \dots, (x_n, y_n)$  

---

### Gesucht:

$$s(x) =
\begin{cases}
P_0(x), & x_0 \leq x < x_1 \\
P_1(x), & x_1 \leq x < x_2 \\
\vdots & \\
P_{n-1}(x), & x_{n-1} \leq x \leq x_n
\end{cases}$$


mit  : 
$P_i(x) = a_{i,0} + a_{i,1} (x - x_i) + a_{i,2} (x - x_i)^2 + a_{i,3} (x - x_i)^3$
$(i = 0, 1, \dots, n-1)$


---

### Gesucht:
**$4n$ unbekannte Koeffizienten:**  
$a_{i,0}, a_{i,1}, a_{i,2}, a_{i,3} \quad (i = 0, 1, \dots, n-1)$

###### Natürliche Spline falls:
$s''(x_{0})=s''(x_{n})=0$

![[Pasted image 20250127175722.png]]