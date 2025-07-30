## Transinformation $H_{T}$
Sie quantifiziert die Menge an Information, die zwei Zufallsvariablen über einander teilen. Genauer gesagt, misst die Transinformation, <span style="color:#ffff00">wie viel Wissen über eine Zufallsvariable durch die Kenntnis einer anderen Zufallsvariable erlangt werden kann.</span>
#### Einheit => $\frac{bit}{Kanalzeichen}$

- ist die Informationsmenge, die im Mittel durch ein Kanalzeichen vom Sender zum Empfänger  übertragen werden kann 


### Im ideal Fall
$$
H(X)=H(Y)=H_{T}
$$

### Durch Störungen:
[[Irrelevanz]]
####  Äquivokation:
wird ein Teil der Information verloren, was mit der Äquivokation bezeichnet wird
=> Nur ein Teil der Information am Kanaleingang erreicht den Kanalausgang

$$
H_{T}= H(X)-H(X|Y)
$$
- [[Markow -  Entropie]]

## Irrelevanz:
Neben der Transinformation enthält die Entropie am Kanaleingang, Störungen auf dem Kanal (Störentropie)
- [[Markow -  Entropie]]
$$
H(Y)=H_{T}+H(Y|X)
$$
$$
H_{T}=H(Y)-H(Y|X)
$$


#### Mit: 
$$
\begin{gather}
H(Y|X)=-\sum_{i}p(x_{i})\sum_{j}p(y_{j}|x_{i})ld\ p(y_{j}|x_{i})\\
H(X|Y)=-\sum_{j}p(y_{j})\sum_{i}p(x_{i}|y_{j})ld\ p(x_{i}|y_{j})
\end{gather}
$$
---
