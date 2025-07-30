- Jedes **Kanalkodewort** $a$ **muss** in seiner Polynomdarstellung durch $g(x)$ **teilbar sein**

	- **Empfangsfolge** $b(x)$ durch $g(x)$ **teilbar** => dann $b \in A$
		- sonst $b \not \in A$ <=> *Fehlererkannt* 
---
### Mit Sicherheit erkennbare Fehler:
-[[Bündelfehler]]
$$
\begin{gather}
f_{e}=d_{min}-1\\
f_{e}=d_{E}-1
f_{b}\leq k
\end{gather}
$$
- $f_{b}$ => **Abstand zwischen erstem und letztem verfälschten Element** $\leq k$

## ALLE $e \not \in A$ erkennbar
---
## Fehlerpolynom
$$
s(x)=b(x) \text{ mod }g(x)=0
$$
- falls $s(x)=0$ => $b \in A$ (*oder Fehler nicht erkannt*)
- falls $s(x)\neq0$ => $b \not \in A$ (**Fehler erkannt**)
### Prüfung ob ein Kodewort im Alphabet liegt
- <span style="color:#00ff04">lo que esta en el recuadro deberia ser una division </span>
![[WhatsApp Image 2024-07-19 at 17.17.01.jpeg]]