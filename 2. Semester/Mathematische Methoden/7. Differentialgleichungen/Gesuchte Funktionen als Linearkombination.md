$$
y=P\cdot u
$$
mit => 
- $P$ besteht aus Eigenvektoren der Matrix $A$
$$
y=
\begin{pmatrix}
y_{1}(x)\\
\dots \\
y_{n}(x) 
\end{pmatrix}
, \quad u=
\begin{pmatrix}
u_{1}(x)\\
\dots \\
u_{n}(x)
\end{pmatrix}
, \quad P=
\begin{pmatrix}
P_{11}& \dots & P_{1n}\\
\dots \\
P_{n1}&\dots& P_{nn}
\end{pmatrix}

$$

#### dann folgt:
$$
y'=P\cdot u'
$$
und:
$$
P\cdot u'=A\cdot P\cdot u
$$

### Bemerkung
- $P^{-1}$ existiert 
- $P^{-1}\cdot A\cdot P$ ist eine **Diagonalmatrix**
$$
u'=(P^{-1}\cdot A\cdot P)\cdot u
$$