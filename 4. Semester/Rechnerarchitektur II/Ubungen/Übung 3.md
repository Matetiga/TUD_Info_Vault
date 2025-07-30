## 3.1
![[Pasted image 20250423093232.png]]

- *Die statische Leistungsaufnahme eines Prozessors kann sich während der Ausführung eines Programmes ändern, auch wenn P-States, Temperatur und C-States konstant bleiben* -> Falsch, da es statisch ist 
- *Die dynamische Leistungsaufnahme eines Prozessors kann sich während der Ausführung eines Programmes ändern, auch wenn P-States, Temperatur und C-States konstant bleiben.* -> Ja, da der Prozessor mehr Energie beim Arbeiten braucht
- *Je mehr Kerne in einem tiefen Schlafzustand (hohen C-State) sind, umso höher können andere Kerne takten.* --> Ja, da wenn ein Kern sein Budget nicht nutzt, kann ein anderer Kerna das Budget haben und ggf. höher takten 

---
## 3.2
### 3.2.1 TDP
Die *Thermal Design Power* (**TDP**) entspricht am ehesten  der nötigen Kühlleistung, die ein System zur Verfügung stellen muss, um einen Prozessor stabil zu betreiben.


	### 3.2.3
- mit $\gamma=\alpha \cdot C$
$$
\begin{gather}
P_{total}=\gamma \cdot f \cdot V^{2} + \beta \cdot V\\
(I) \quad 100W=\gamma \cdot 2GHz \cdot 1,4^{2}V^{2} + \beta \cdot 1,4V \\
(II) \quad 90W=\gamma \cdot 1GHz \cdot 1,4^{2}V^{2} + \beta \cdot 1,4V \\
(I-II) \quad 10W=\gamma 1GHz \cdot 1,4^{2} V^{2}
\end{gather}
$$
 dann bekommt man: 
- $\gamma=5,1\cdot 10^{-9} \frac{As}{V}$
- $\beta=57,14A$

*Die TDP des Prozessors beträgt 120 W. Kann der Prozessor während er den gleichen Workload ausführt dauerhaft auf 2.4 GHz bei 1.6 V hochtakten?*
- Nein, da
$120W \not> 122,78W=\gamma \cdot 2.4GHz \cdot 1,6^{2}V^{2} + \beta \cdot 1,6V$


*Nehmen Sie an, dass der Prozessor 4 Kerne und zusätzliche geteilte Ressourcen hat, die er bislang auch genutzt hat. Die dynamische Leistungsaufnahme aus der Vorrechnung kann gleichmäßig den Kernen zugeschlagen werden, ebenso wie jeweils 15% der statischen Leistungsaufnahme. Die restlichen 40% der ermittelten statischen Leistungsaufnahme werden von den gemeinsam genutzten Ressourcen gebraucht.*

*Nehmen Sie weiterhin an, dass die Ausführungszeit für ein Programm perfekt mit der Prozessorfrequenz skaliert (Verdopplung der Frequenz entspricht Halbierung der Laufzeit) und zusätzlich noch perfekt parallel ist (Verdopplung der Kernanzahl halbiert die Laufzeit*

- mit : $C$ : Core
$$
\begin{gather}
t_{4C,1GHz}=\frac{1}{2}t_{1C,2GHz} \\
P_{4C,1GHz} = P_{dyn}+P_{static}= 62,2W \\
P_{1C,2GHz} = 0,25\cdot 20W + 0,55\cdot 80W = 49W
\end{gather}
$$
Daraus kann man die Watts einsetzen um die Energie zu bestimmen 
$$
\begin{gather}
E_{4C,1GHz}=62,2W \cdot t_{4C,1GHz} \\
E_{1C,2GHz}=49W \cdot 2\cdot t_{4C,1GHz} \\
\end{gather}
$$
- Also $E_{4C,1GHz}$ braucht weniger Energie

---

## 3.3
### 3.3.2
*Im nächsten Schritt soll eine Taktsenkung via DVFS nur für manche Regionen angewendet werden. Für welche wäre es geeignet, wenn das Anfordern einer neuen Frequenz jeweils einen Overhead von 10 ms bei 100 W bedeutet und einmal auf eine neue Frequenz gewechselt werden muss?*

 **Foo** : ja, da 
- $0,7s\cdot 120 W=84J$ (*default*)
- $0,8 \cdot 100W=80J$ (*DVFS*)
	- also DVFS besser da, $80J > 84J$


#### Energie Optimum 
- bei $10GB$
$$
E=100(E_{DVFS-switch} + E_{foo-DVFS}+E_{bar-DVFS}+E_{DVFS-switch} + E_{baz})
$$
$$
E=100(1J+0,8s \cdot 100W+0,31s \cdot 95W + 1J+ 0,7s \cdot 105W)= 18495J
$$

