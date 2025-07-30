[[Orthogonalprojektion]]

Sei $V$ ein Vektorraum indem Skalarprodukt $\bullet$ definiert ist
Sei $U$ ein Untervektorraum von $V$

- Jede Vektor $v \in V$ hat die Form:
  $$
  v=\hat{v}+w
$$
- $\hat{v}\in U$
- $w\in U^{\perp}$

---

### Gegeben:
- $\{ u_{1},u_{2},\dots u_{k} \}$ Ortogonalbasis von $U$, dann gilt:
- [[Orthogonalprojektion]] *mit jedem Orthogonalbasisvektor*
$$
\hat{v}=\text{proj}_{U}v=\frac{v \bullet u_{1}}{ui \bullet u_{1}}u_{1}+\frac{v\bullet u_{2}}{u_{2} \bullet u_{2}}u_{2}+\dots \frac{v\bullet u_{k}}{u_{k} \bullet u_{k}}u_{k}
$$

##### $\hat{v}$ ist die Bestapproximation von $v \in V$ durch ein Element von $U$
---
#### Beispiel
$$
 \text{ proj}_{\text{Span}(\{ b_{1} \})}u_{2}=\frac{u_{2} \bullet b_{1}}{b_{1} \bullet b_{1} }b_{1}
$$