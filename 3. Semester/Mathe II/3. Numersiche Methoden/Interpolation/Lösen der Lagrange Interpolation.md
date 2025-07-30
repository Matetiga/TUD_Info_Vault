**Lagrange-Polynome**  aufstellen :
- $L_0(x), L_1(x), \dots, L_n(x)$

### Ansatz: 
$p(x) = a_0 \cdot L_0(x) + a_1 \cdot L_1(x) + \dots + a_n \cdot L_n(x)$

**Ermittlung** von $a_0, a_1, \dots, a_n$ mit Hilfe der **Interpolationsbedingungen**:  $y_i = p(x_i) = a_0 \cdot L_0(x_i) + \dots + a_{i-1} \cdot L_{i-1}(x_i) + a_i \cdot L_i(x_i) + a_{i+1} \cdot L_{i+1}(x_i) + \dots + a_n \cdot L_n(x_i)$ 
- mit $L_{i}(x_{i})=1$ und alles anderes mit $\neq i$ ist $=0$ (aus [[Lagrange Interpolation]])
### somit folgt:
$\Rightarrow y_i = a_i \quad (i = 0, 1, \dots, n)$
**Damit ist das LGS bereits gelöst.**
$$p(x) = \sum_{k=0}^n y_k \cdot L_k(x)$$

**Lagrange-Interpolationspolynom der Ordnung $n$**

---

### Beispiel
- $(x_{i},y_{i}) \quad (i=0,1,\dots,n)$
- somit folgt : $y_{k}=\{ -3,1,2,7 \}$
- beachte, dass für jedes [[Lagrange Interpolation]] Polynom $k \neq i$ gilt 

![[Screenshot from 2024-12-16 16-36-15.png]]