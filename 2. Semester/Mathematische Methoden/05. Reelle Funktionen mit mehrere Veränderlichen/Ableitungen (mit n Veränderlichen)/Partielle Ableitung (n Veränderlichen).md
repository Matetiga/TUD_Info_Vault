### Unterschied - partielle und totaler Differenzierbarkeit
- [[Totaler Differenzierbarkeit]] => Funktionen, die linear approximierbar sind. Die Lineare Näherungsformel wird mit Hilfe der Grandient der Funktion gemacht
- [[Partiell Differenzierbar]]: Vektorwertige Funktionen. Wird mit Hilfe der Jacobi-Matrix aufgestellt -> Dann wird für totale differenzierbare Funktionen die lineare Näherungsformel  angegeben


---

Sei $x \subseteq \mathbb{R}^{n}$ eine Offene Menge
$$
f:X\to \mathbb{R}^{1} \text{ heisst in } x_{0}=(\hat{x}_{1}, \dots, \hat{x}_{n})\text{ partiell nach }x_{i} \text{ differenzierbar}
$$
wenn die Partielle Funktion
$$
f_{i}:\mathbb{R}\to \mathbb{R}:x\to f(x_{1},x_{2},\dots,x_{i-1}, x, x_{i+1},\dots,x_{n}) \text{ in }\hat{x}_{i}\text{ differenzierbar ist}
$$
---
## Bezeichnung
#### $$\frac{ df}{ dx_{1}}(x_{0}):=f'_{i}(\hat{x}_{i})$$
##### heisst: partielle Ableitung von $f$ nach $x_{i}$ an der Stelle $x_{0}$
- Man ableitet $f$ nach $x_{i}$
- alle andere Variablen werden als Konstanten betrachtet
- Ableitungsregeln sind anwendbar
---


# Partielle Ableitung 2. Ordnung
- Wird mit Hilfe der partielle Ableitung 1. Ordnung gemacht 

### Beispiel
$f(x,y)=x^{2}y-e^{yx}$

##### Partielle Ableitung nach x:
$$
f_{x}(x,y)=\frac{df}{dx}(x,y)=y\cdot 2x-e^{xy}y
$$
##### Partielle Ableitung nach y:
$$
f_{y}(x,y)=\frac{df}{dx}(x,y)=x^2\cdot 1-e^{xy}x
$$
#### Partielle Ableitung 2. Ordnung:
$$
f_{xy}(x,y)= \frac{d}{dy} \frac{df}{dx}(x,y)= \frac{d^{2}f}{dy \ dx}(x,y)=2x-e^{xy}x\cdot y -e^{xy}\cdot 1
$$
- Hinweis: Produktregel für => $e^{xy}\cdot x$

---

