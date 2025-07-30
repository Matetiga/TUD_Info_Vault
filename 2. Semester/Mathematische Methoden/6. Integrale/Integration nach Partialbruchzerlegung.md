https://studyflix.de/mathematik/partialbruchzerlegung-1499
### Für Rationale Funktionen
$$
R(x)= \frac{A(x)}{Q(x)}
$$
- A(x) und Q(x) sind Polynomfuntkionen
-  Grad $A(x) >$ Grad $Q(x)$ => dann muss man was im **1. Schritt** passiert **machen**
#### Falls  Grad $A(x) \ngtr$ Grad $Q(x)$ 
dann gilt (Beispiel) =>
- ein <span style="color:#ffff00">irreduzibler quadratische Faktor</span> hat die Formel $\frac{Ax+B}{x^2+bx+c}$
$$
\frac{x^{2}-9}{(x^{2}+1)(x-2)}=\frac{Ax+B}{x^{2}+1}+\frac{C}{x-2}
$$

#### Bemerkung:
- alle haben derselbe Nenner aber mit einr grösseren Exponent
$$
\frac{x^{2}-9}{(x-2)^{3}}=\frac{A}{(x-2)}+\frac{B}{(x-2)^{2}}+\frac{C}{(x-2)^{3}}
$$

---

## 1. Schritt
$\text{mit } A(x)=B(x)\cdot Q(x)+P(x)$
-  Grad $P(x) <$ Grad $Q(x)$ => <span style="color:#ffff00">dann</span> **kann man Polynomdivision machen**

$$
R(x)=B(x)+ \frac{P(x)}{Q(x)}
$$

## 2. Schritt: Partialzerlegung vorbereiten
### Nullstellen bestimmen 
- Q(x) => in Faktoren zerlegen
#### Zerlegung der Faktoren 
- man muss die Nullstellen von $Q(x)$ in $\mathbb{C}$ finden
- 
 $$
Q(x)=(x−a_{1})^{n_{1}}(x−a_{2​})^{n_{2}}…(x−a_{k}​)^{n_{k}}
$$

## 3. Schritt: Partiallzerlegung Durchführen
- (unten im Bruch) stehen nur **irreduzieren Faktoren** (*Nenner kann nicht weiter faktorieziert werden*)

- <span style="color:#ffff00"> Um die Koeffizienten</span> $A_{1},A_{2}\dots A_{k}$ <span style="color:#ffff00">zu bestimmen, muss man mal</span> $Q(x)$ <span style="color:#ffff00">multiplizieren </span>
$$
\frac{P(x)}{Q(x)}=\frac{A_{1}}{x-a_{1}}+\frac{A_{2}}{x-a_{2}}+\dots+\frac{A_{k}}{x-a_{k}}
$$

---
# Beispiel
$$
\frac{x+1}{(x-1)(x-2)}
$$
#### Zerlegung des Nenners
$$
(x-1)(x-2)
$$

#### Partialbruchzerlegung
$$
\frac{x+1}{(x-1)(x-2)}=\frac{A}{(x-1)}+\frac{B}{(x-2)}
$$
$$
\begin{gather}
x+1=A(x-1)+B(x-1)\\
\Leftrightarrow x+1=Ax-2A+Bx-B\\
\Leftrightarrow x+1=(A+B)x-(2A+B)\\
\end{gather}
$$
##### Dann muss man die Koeffizienten der beiden Seiten vergleichen und in Gleichungen trennen
###### 1. Glecihung
$x=(A+B)x$

###### 2. Gleichung
$1=-2A-B$

##### Dann folgt:
$$
\begin{gather}
x=(A+B)x \Leftrightarrow 1= A+B \Leftrightarrow 1-A=B\\
\text{somit folgt: }\\
1=-2A-B \Leftrightarrow 1=-2A-(1-A) \Leftrightarrow -2=A\\
\text{und somit:}\\
1=A+B \Leftrightarrow 1=-2+B \Leftrightarrow B=3
\end{gather}
$$

#### Alles zusammengesetzt:
$$
\frac{x+1}{(x-1)(x-2)}=\frac{-2}{(x-1)}+\frac{3}{(x-2)}
$$
---

# Integration

$$
\int R(x) \, dx = \int B(x) \, dx + \int \frac{P(x)}{Q(x)} \, dx 
$$

---

