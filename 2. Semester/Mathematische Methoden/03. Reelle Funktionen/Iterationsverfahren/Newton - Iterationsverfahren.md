Mit Hilfe der:
- 1. Ableitung
- 2. Ableitung

## Iterationsform 

$$ 
x:= x-\frac{f(x)}{f'(x)} \quad bzw \quad x_{n+1}:=x_{n}-\frac{f(x_{n})}{f'(x_{n})}
$$
mit Startwert $x_{0}$


#### Anwendung zur Iteration des n-ter Wurzer
mit $x_{^{n}=a}\Leftrightarrow f(x)=x^{n}-a=0$
$$
x:= \frac{1}{n}\left( (n-1)*x+\frac{a}{x^{n-1}} \right)
$$

---
## Konvergenz Bedingungen:
$$
| \frac{f(x)*f''(x)}{(f'(x))^{2}}|<1
$$

#### Beispiel:
mit $x^{*}=2.1$ (Startwert)
$$
f(x) = x^{3} -5x +1 = 0
$$
$$
x:= x-\frac{x^{3}-5x+1}{3x^{2}-5}
$$
$$
|g'(2.1)|=|\frac{f(2.1)*f''(2.1)}{(f'(2.1))^{2}}|=0.04
$$
=> also **gute konvergenz**

