## $G_{l \times n}$
- mit $l$ linear unabhängige Kanalkodewörter
- mit $L=2^l$ (totale Anzahl an Kanalkodewörter)

#### Einheitsmatrix über den ersten $l$ Spalten
- $G_{l \times n}=[I_{l}C]$
	- $I_{l}$ => Einheitsmatrix
	- $C$ => Redundanter Stellen


$$
G_{l\times n}=
\begin{pmatrix}
1&0&0&\dots& 0& u_{1,l+1}&u_{1,l+2}&\dots& u_{1,n} \\
0&1&0&\dots& 0& u_{2,l+1}&u_{2,l+2}&\dots& u_{2,n} \\
\dots \\
0&0&0&\dots& 1& u_{l,l+1}&u_{l,l+2}&\dots& u_{1l,n}
\end{pmatrix}
$$

![[WhatsApp Image 2024-06-11 at 16.21.27.jpeg]]

---

## Kodewort generieren

$$
a_{i}=a^{*}\cdot G
$$
- $a^{*}$ ist ein $l$-Lang Informationswort
- $G_{l \times n}$
