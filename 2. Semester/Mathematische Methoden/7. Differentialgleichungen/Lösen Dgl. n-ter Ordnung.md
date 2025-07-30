## Gesucht
$$
y^{(n)}=f(x,y,y',\dots,y^{(n-1)})
$$
### 1. Schritt
- Setze: 
- $y_{1}:=y$
- $y_{2}=y'$
- ...
- $y_{n}=y^{(n-1)}$

#### Bilde jeweils die Ableitung
$$
\begin{gather}
y'_{1}=y_{2}\\
y'_{2}=y_{3}\\
\dots\\
y'_{n-1}=y_{n}\\
y_{n}=f(x,y_{1},\dots,y_{n})
\end{gather}
$$
=> Aus der Lösung des Systems, kann man die Lösung der Dgl. ablesen
$$
y(x)=y_{1}(x)
$$


### Beispiel
- gesucht $y(x)$
$$
\begin{gather}
y''=-2y+3y'\\
y_{1}= y \\
y_{2}=y'\\
y_{2}'=y''=-2y+3y'\\
\text{ somit folgt: } \\
y_{1}'=y_{2}\\
y_{2}'=-2y_{1}+3y_{2}
\end{gather}
$$
- daraus kann man eine Matrix bilden:
$$
\begin{pmatrix}
y_{1}' \\
y_{2}'
\end{pmatrix}
=
\begin{pmatrix}
0 & 1 \\
-2 & 3
\end{pmatrix}
\begin{pmatrix}
y_{1} \\
y_{2}
\end{pmatrix}
$$

