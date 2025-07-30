$$
(n,l,d_{min}) \to(n-?,l-?,d_{min})
$$
- mit $k$ => **konstant**
- <span style="color:#ffffff">Zyklische Eigenschaft, Fehlererkennung und Fehlerkorrekur </span>**bleiben erhalten**

---

### Beispiel
- $l=12$
- $d_{E}=5$
	- somit folgt => $\mu =1$
	- $\mu + d_{e}-2=4$
		- $g(x)=\text{kgV}\{ m_{1}(x),m_{2}(x),m_{3}(x),m_{4}(x) \}=m_{1}(x)\cdot m_{3}(x)$

#### $k_{1}$ Abschätzung
$$\begin{gather}
n_{max}=2^{k_{1}}-1\geq l+k\\
\text{ mit }k_{1}=3 \text{ folgt }\implies 7 \not \geq 12+k \\
\text{ mit }k_{1}=4 \text{ folgt }\implies 15\geq 12+ k
\end{gather}$$
- Dann muss man bestimmen ob diese Ungleichung mögich wäre
	- **also k bestimmen** 
	- man muss <span style="color:#ffff00">Zyklen bestimmen </span>
- mit $\alpha^{2^{i} \text{ mod }n_{max}}$
- in diesem Fall wäre $n_{max}=15$
$$
\begin{gather}
m_{1}(x)=\alpha^{1}, \alpha^{2}, \alpha^{4}, \alpha^{8}, \alpha^{16 \text{ mod }15 =1} \implies \text{ grad }=4 \\
m_{3}(x)=\alpha^{3}, \alpha^{6}, \alpha^{12}, \alpha^{24 \equiv 9}, \alpha^{18 \equiv 3}  \implies \text{ grad }=4
\end{gather}
$$
- somit ist $k= \text{ grad }m_{1}(x)+\text{ grad }m_{3}(x)=8$
- **Aber dann folgt:**
$$
\text{ mit }k_{1}=4\implies 15 \not \geq 12+8
$$
##### Dann muss man weiter mit $k_{1}$ probieren
- mit $k_{1}=5$
- dann folgt: $31\geq 12+k$

**Wieder Zyklen bestimmen** 
$$
\begin{gather}
m_{1}(x)=\alpha^{1}, \alpha^{2}, \alpha^{4}, \alpha^{8}, \alpha^{16}, \alpha^{32 \text{ mod }31=1} \implies \text{ grad }=5 \\
m_{3}(x)=\alpha^{3}, \alpha^{6}, \alpha^{12}, \alpha^{24}, \alpha^{48 \equiv 17}  \implies \text{ grad }=5
\end{gather}
$$
- somit ist $k= \text{ grad }m_{1}(x)+\text{ grad }m_{3}(x)=10$
- **Dann folgt:**
$$
\text{ mit }k_{1}=5=31\geq 12+10
$$

#### Dann folgt:
$l+k=n \Leftrightarrow 12+10=22$
$d_{min}=5$ *würde von der Aufgabe gegeben*
### Somit: $(31,12,5)\text{BCH} \to (22,12,5)\text{BCH}_{Verkleinert}$
