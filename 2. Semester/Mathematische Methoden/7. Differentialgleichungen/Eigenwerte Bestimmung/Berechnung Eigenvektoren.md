## Eigenvektor
- Der Eigenvektor $v$ wird *Eigenvektor de Matriz zum Eigenwert* $k$ gennant

Eine Matrix $A \in K^{n\times n}$ hat genau den Eigenwert $k \in K$ wenn
$$
\det(A-kE_{n})=0
$$
- [[Berechnung Eigenwerte]]

---

### Man muss den Kern von $(A-kE_{n})$ bestimmen
#### Beispiel

$$
A=
\begin{pmatrix}
1 & 3 \\
0&4
\end{pmatrix}
$$
$\text{ Eigenwerte der Matrix A sind: } k_{1}=1, \quad k_{2}=4$
- [[Berechnung Eigenwerte]]

###### mit $k_{1}=1$
$$
Eig_{1}(A)=ker(A-1\cdot E_{2})
$$
$$
\begin{pmatrix}
1-1&3 \\
0&4-1
\end{pmatrix}=
\begin{pmatrix}
0 & 3 \\
0 & 3
\end{pmatrix}=
\begin{pmatrix}
0&1 \\
0&0
\end{pmatrix}
$$
$$
Eig_{1}(A)=Spann(\{ \begin{pmatrix}
1 \\
0
\end{pmatrix} \})
$$
###### mit $k_{2}=4$
$$
Eig_{4}(A)=ker(A-4\cdot E_{2})
$$$$
\begin{pmatrix}
1-4&4 \\
0&4-4
\end{pmatrix}=
\begin{pmatrix}
-3&-3 \\
0&0
\end{pmatrix}=
\begin{pmatrix}
-1&-1 \\
0&0
\end{pmatrix}=
$$
$$
ker\begin{pmatrix}
-1&-1 \\
0&0
\end{pmatrix}=
-x+y=0 \quad \quad \text{mit } y=t \implies t\begin{pmatrix}
1 \\
1
\end{pmatrix}
$$
