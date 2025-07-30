Die von einer [[Grammatik]] $G= \langle V, \Sigma, P, S \rangle$ erzeugte Sprache **besteht aus allen Wörtern über** $\Sigma$, die man von $S$ ableiten kann ([[Ableitungsrelation =>*]])
- es ist eine Menge aus die mögliche erzeugbare Wörte

$$
L(G)=\{  w\in \Sigma^{*}| S\implies^{*}w \}
$$

---

### Beispiel 
- **klein Buchstaben** sind *Terminalsymbole*
- **groß Buchstaben** sind *Variblen*
mit $G_{id}$ :
$S\to BA \quad A \to BA|ZA|\epsilon \quad B\to b \quad Z\to z$

dann gilt für: $L(G_{id})=\{ b \} \circ \{ b,z \}^{*}$