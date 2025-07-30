##  Schritte
- man bestimmt mit Fano/Huffman für Wörter der Länge 2
- dann bestimmt man $l_{m}$ mit den geraden erstellten $l_{i}$ 
- Falls das die Bedingung erfüllt => $\checkmark$


---
### Beispiel:
$p(A)=0.8$
$p(B)=0.2$
- Man bestimmt die Fano/Huffman von AA, AB, BA, BB

- dann bestimmt man $$l_{m}^{[2]}=\sum^{N^{m}}_{j=1}p(x_{j}^{[2]})l_{j}^{[2]}=1,56$$
$$
l_{m}=\frac{l_{m}^{[2]}}{m}=\frac{1,56}{2}=0.78
$$


- Wir wollen eine Optimalkodierung von *mindestens 25%*
	- aber $0.78\not\leq0.75$
	
- somit bestimmt man Fano/Huffman **mit der Länge 3**  
	- dann folgt:
		$l^{[3]}_{m}=2,184 \frac{KZ}{Block}$
		$l_{m}=0,728 \frac{KZ}{QZ}$
