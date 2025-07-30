Hilft zur Integrieren mit [[Integration nach Partialbruchzerlegung]]
#### Wenn Grad des Zählers grösser als der Grad des Nenners ist

$$
\int B(x)+ \frac{A(x)}{Q(x)} \, dx 
$$

---
### Beispiel
- $\text{ Grad }P(x) > \text{ Grad } Q(x)$
$$
\int \frac{x^{3}-2x^{2}-2x-27}{x^{2}-2x-3} \, dx 
$$
**1. Schritt**
- hochste Grad von $P(x)$ durch hochste Grad von $Q(x)$ <span style="color:#ffff00">teilen </span> 
- => $B(x)$
$$
x^{3} : x^{2}=x
$$

**2. Schritt**
- Lösung 1. Schritt mit $Q(x)$ **multiplizieren**
$$
x^{3}-2x^{2}-3x
$$

**3. Schritt**
- $P(x) - Q(x)=A(x)$
$$
(x^{3}-2x^{2}-2x-27)-(x^{3}-2x^{2}-3x)=x-27
$$
**4. Schritt**
- alles zusammensetzen 
- (<span style="color:#ffff00"> wenn das Grad des Zählers noch grösser als der des Nenners ist,  muss man wieder von 2. Schritt weiter machen</span>)
$$
\int x+\frac{x-27}{x^{2}-2x-3} \, dx 
$$