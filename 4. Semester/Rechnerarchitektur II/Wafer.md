## Dies Per Wafer Formel 
 $$
 \frac{A_{wafer}}{A_{die}}-\frac{\pi\cdot d_{wafer}}{\sqrt{ 2\cdot A_{die} }}
$$
![[IMG_2760.jpeg]]

---
## Defekts Per Area Formel
$$
yield_{die}=yield_{wafer}* \frac{1}{(1+defekPerArea*A_{die})^{n}}
$$
Dann muss man $yield_{wafer}$ mit der Anzahl an Dies **multiplizieren**:
$$
Funktionierende_{Dies} = diesPerWafer \cdot yield_{wafer}
$$

---
## Aufgaben
Sie möchten Prozessoren zu einem bestimmten Preis herstellen. Dabei können Sie sich entscheiden Prozessoren mit einem großen Cache oder einem kleinen Cache zu produzieren. Beide Prozessoren werden aus dem gleichen Wafer hergestellt. Die Dies der quadratischen Prozessoren haben eine **Kantenlänge von 12 mm** (*kleiner Cache*) beziehungsweise **16 mm** (*großer Cache*). Der Wafer hat einen **Durchmesser von 280 mm und einen yield von 0,99**
### Anzahl an Dies Per Wafer
- Wieviele kleine Dies passen auf einen Wafer? 375
$$\frac{\pi \cdot 140^{2}mm^{2}}{12^{2}mm^{2}}-\frac{\pi \cdot 280mm}{\sqrt{ 2*12^{2}mm^{2}}}=375$$
- Wieviele große Dies passen auf einen Wafer? 201

### Anzahl an funktionierende Dies
Wieviele funktionierende Dies bekommen Sie im Durchschnitt pro Wafer, wenn die **Prozesskomplexität 15,5 beträgt und 0,020 Fehler pro cm²** auftreten?
- Für kleiner Dies : 
$$375 \cdot 0,99\cdot \frac{1}{\left( 1+0,02cm^{2}\cdot \frac{12^{2}}{100} \right)^{15,5}} = 239,1$$
	- <span style="color:#ffff00"> Wichtig</span>: $A_{dies} = 12^{2}mm^{2}$, ich weiss nicht wieso es nur durch 100 geteilt wird und nicht durch 10000, um es in $cm^{2}$ umzuformen
- Für großere Dies : $91,8$

