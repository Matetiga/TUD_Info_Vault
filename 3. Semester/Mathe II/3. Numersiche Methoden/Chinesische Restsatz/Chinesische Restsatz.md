## Chinese Remainder Theorem (CRT)
Seien $m_1, \dots, m_t \in \mathbb{N} \setminus \{0, 1\}$ [[#paarweise teilerfremd]] und $b_1, \dots, b_t \in \mathbb{Z}$.  
Dann gibt es modulo $m$ mit $m := m_1 * \dots * m_t$ genau ein $x$ mit
$$
\begin{gather}
x \equiv b_1 \pmod{m_1}  \\
\vdots  \\
x \equiv b_t \pmod{m_t}  
\end{gather}
$$

**Nämlich:**  
$x = a_1 \cdot x_1 + \dots + a_t \cdot x_t \pmod{m}$
Wobei:  
- $a_j := \frac{m}{m_j} \quad (j = 1, \dots, t)$  
- $a_j \cdot x_j \equiv b_j \pmod{m_j} \quad (j = 1, \dots, t)$  
erfüllt ist.
---
##### paarweise teilerfremd
mit : $m_1, \dots, m_t \in \mathbb{N} \setminus \{0, 1\} \Leftrightarrow \text{ggT}(m_{i},m_{j})=1 \quad \forall i,j \in \{ 1,\dots,t \} \text{ und } i \neq j$
![[Screenshot from 2024-12-09 12-30-36.png]]