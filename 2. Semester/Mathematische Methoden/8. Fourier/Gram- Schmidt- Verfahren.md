## Gegeben
- Basis eines UVR  $U \quad \{u_{1},u_{2},\dots u_{t}  \}$ des $\mathbb{R}^{n}$

#### Gesucht
- **Orthogonalbasis $\{ b_{1}, b_{2}, \dots b_{t} \}$ von U**

---

### Verfahren:
$$
\begin{gather}
b_{1}:=u_{1}\\
b_{2}:=u_{2}- \text{ proj}_{\text{Span}(\{ b_{1} \})}u_{2}\\
b_{3}:=u_{3}- \text{ proj}_{\text{Span}(\{ b_{1},b_{2} \})}u_{3}\\
\dots\\
b_{t}=u_{t}- \text{ proj}_{\text{Span}(\{ b_{1},b_{2},\dots,b_{t} \})}u_{t}
\end{gather}
$$
- mit $\text{ proj}_{\text{Span}(\{ b_{1} \})}u_{2}$ => [[Orthogonalzerlegung]]
---

## Bemerkung
- Wenn man **wieder das Gram- Schmidt verfahren auf ein Vektor benutzt**, welchel<span style="color:#ffff00"> lin. unabhängig </span>und <span style="color:#ffff00">schon durch den Verfahren einmal eingegangen </span>ist, **dann bekommt man den Nullvektor**
