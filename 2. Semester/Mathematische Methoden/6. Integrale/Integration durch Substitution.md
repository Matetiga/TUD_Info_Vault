#### Stamm aus der Kettenregel
$$
\int f'(g(x))\cdot g'(x) \, dx =f(g(x))+c
$$

## Substitution
- $dz$ muss die Ableitung von $z$ sein
$$\begin{gather}
z:=g(x)\\
dz:=g'(x) \ dx
\end{gather}$$
=> dann gilt
$$
\int f'(g(x))\cdot g'(x) \, dx =\int f'(z) \, dz =f(z)+c=f(g(x))+c
$$

---

### Beispiel
$$
\begin{gather}
\int  \frac{dx}{x(1+(\ln(x))^{2})} & \text{ mit } z:=\ln(x) \text{ und  } dz:= \frac{1}{x}dx \\ \\

=\int \frac{dz}{a+z^{2}}\\ \\
= \arctan(z)+c\\ \\
=\arctan(\ln(x))+c

\end{gather}
$$