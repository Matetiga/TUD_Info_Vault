Pump-Eigenschaft **notwendig, aber nicht hinreichend** für *Kontextfreiheit*
### Satz (Pumping-Lemma):
L ist kontextfrei $\implies$ **Pumpbar ab Pumpingzahl**
Für jede kontextfreie Sprache $\mathcal{L}$ gibt es eine Zahl $n \geq 0$, so dass gilt:
-  Für jedes Wort $z \in \mathcal{L}$ mit $|z| \geq n$ gibt es eine Zerlegung:
	- $z = uvwxy$ mit $|vx| \geq 1$
	- und $|vwx| \leq n$, so dass: Für jede Zahl $k \geq 0$ gilt: $uv^kwx^ky \in \mathcal{L}$.
	- [[Ableitungsbäume aufpumpen]]

---
## Beispiel:
Für die Sprache $\{a^ib^i \mid i \geq 0\}$ gilt der Satz.

**Beweisansatz:**  
Wir müssen ein $n$ präsentieren, für das die Aussage des Lemmas gilt.  
Wir wählen $n = 2$. Sei $z = a^ib^i$ mit $i \geq 1$ ein beliebiges Wort mit $|z| \geq 2$.

**Idee:**  
Beim Aufpumpen sollen möglichst genau so viele $a$s wie $b$s erzeugt werden.  
Wir wählen die Zerlegung $u = a^{i-1}, \ v = a, \ w = \epsilon, \ x = b, \ y = b^{i-1}$.  

Dann ist $uv^kwx^ky = a^{i-1}a^kb^kb^{i-1} = a^{i+k-1}b^{i+k-1} \in \mathcal{L}$ für alle $k \geq 0$.
