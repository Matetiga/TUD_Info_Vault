Komplexitätsklassen sind Mengen von Sprachen, die man (grob) einteilt entsprechend
der Ressourcen, die eine TM zur Entscheidung ihres Wortproblems benötigt.
- [[Beziehungen der Komplezitätsklassen]]

## Komplezitätsklassen

| deterministisch |                        | nicht deterministisch |
| --------------- | ---------------------- | --------------------- |
| L = LogSpace    | logarithmischer        | NL = NLogSpace        |
| P = PTime       | polynomielle Zeit      | NP = NPTime           |
| PSpace          | polynomieller Speicher | NPSpace               |
| Exp = ExpTime   | exponentielle Zeit     | NExp = NExpTime       |

---
dasselbe gilt für nicht deterministische Komplexitätsklassen
## Unter [[Schranken für Zeit und Raum#DTIME(f(n))|DTime]]

### Polynomielle Zeit 
$$P=\text{ PTime} = \bigcup_{\geq 1}\text{DTime }(n^{d})$$
### Exponentielle Zeit 
$$\text{ Exp}=\text{ ExpTime} = \bigcup_{\geq 1}\text{DTime }(2^{n^{d}})$$

---
## Unter [[Schranken für Zeit und Raum#DSPACE(f(n))|DSpace]]
### Logarithmischer Speicher 
$$\text{ L}=\text{ LogSpace} = \bigcup_{\geq 1}\text{DSpace }(\log(n))$$
Man definiert spezielle speicher beschränkte TMs (Mehrbände TM)
- Der erste Band ist die *Eingabeband* -> Darf **nur gelesen** werden
- Das zweite Band ist das *Ausgabeband* -> Darf **nur geschrieben** werden
	- Dieses Band ist auf $O(\log(n))$ viele Speicherzellen beschränkt 

### Polynomieller Speicher 
$$\text{ PSpace} = \bigcup_{\geq 1}\text{DSpace }(n^{d})$$


