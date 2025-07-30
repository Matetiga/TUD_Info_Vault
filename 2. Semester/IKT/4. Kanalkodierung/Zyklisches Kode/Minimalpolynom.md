- Jede $\alpha^{i}$ ist ein **Minimalpolynom** $m_{i}(x)$ **zugeordnet**
	- Minimalpolynom = [[Irreduzibel Polynom]]
	- Grad $r\leq k_{1}$

$$
\begin{gather}
m_{0}(x)=\alpha^{0}\\
m_{1}(x)=\alpha^{1}, \alpha^{2}, \alpha^{4}, \dots, \alpha^{i \text{ mod p}}\\
m_{2}(x)=\alpha^{2}, \alpha^{4}, \alpha^{8}, \dots, \alpha^{i \text{ mod p}} = m_{1}(x)\\
m_{3}(x)=\alpha^{3}, \alpha^{6}, \alpha^{12}, \dots, \alpha^{i \text{ mod p}}\\
\dots
\end{gather}
$$
- mit $p_{max}=n=2^{k_{1}}-1$ [[0. Wichtige Formeln]]

##### somit folgt: 
$$
\begin{gather}
m_{0}(x)=(x+1)\\
m_{1}(x)=(x+\alpha^1)(x+\alpha^2)(x+\alpha^4)\dots\\
\dots\\
m_{3}(x)=(x+\alpha^3)(x+\alpha^6)(x+\alpha^9)\dots
\end{gather}

$$