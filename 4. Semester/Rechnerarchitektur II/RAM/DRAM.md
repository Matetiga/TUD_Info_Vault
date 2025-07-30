Besteht aus einem Kondensator 
- Transistor verbindet Kondensator und Bitline bei Anwahl durch die Wordline 
- Entladung des Kondensators:
	- Beim Lesen durch Leitungskapazitäten
	- Über Zeit 
	- Deswegen brauch das Matrix *Refresh-Zyklen* auf Speicherzellen
- DRAM hat nur halb so viele Adressanschlüsse wie [[SRAM]] bei gleicher Kapazität
![[Pasted image 20250520130152.png]]

---

## Fehlererkennung 
- Durch Paritätsbit
Einzelfehler können erkannt werden, aber nicht korrigiert 

#### Hamming-Code
Mit einem Hamming-Code kann man alle Einzelbitfehler korrigieren
- [[Hamming Kode - Linearkodes]]
- Formel für Anzahl der Prüfbits $(m+r+1) \leq 2^{r}$
	- $m$ Datenbits
	- $r$ Paritätsbits
- Alle Bits, deren **Bitnummer eine Potenz von 2** ist, sind *Paritätsbits*
- Im Allgemeinen wird Bit b von den Bits $b_{1}, b_{2}, …,b_{j}$ so geprüft, dass $b_{1} + b_{2} + … + b_{j} = b$gilt
- Falls es sein Falschen Paritätsbit gab: 
	- Die **Summe aller falschen Paritätsbits** ist die Position des falschen Bits