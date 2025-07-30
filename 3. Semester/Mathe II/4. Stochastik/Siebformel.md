## Formale Definition 
Für Ereignisse $A_1, A_2, \ldots, A_n$ ($n \geq 2$) aus einem Ereignisfeld $\mathcal{E}$ gilt:  
$$p\left( \bigcup_{i=1}^n A_i \right) = \sum_{i=1}^n p(A_i) - \sum_{i < j} p(A_i \cap A_j) + \sum_{i < j < k} p(A_i \cap A_j \cap A_k) - \cdots$$
$$= \sum_{\ell=1}^n (-1)^{\ell+1} \sum_{i_1 < i_2 < \cdots < i_\ell} p\left( A_{i_1} \cap A_{i_2} \cap \cdots \cap A_{i_\ell} \right)$$

---
### Beispiel

![[Pasted image 20250114124447.png]]