## 08.1 ECC
### 08.1.2 Hamming-Code Teil 2: Codewortberechnung
>[!Question]
>Woher Kommt das Schema, an dem die zu kontrollierende Bits die Patitätsbits zuweisen (Slide 71 Vorlesung 7)

### 08.1.3 Hamming-Code Teil 3: Fehlerhaftes Codewort erkennen
**1**<span style="color:#ffff00">0</span>0<span style="color:#ffff00">0</span> 100**1** 0010 110**0** 1101 1
- blau markierte Bits sind korrekte (gerade) Paritätsbits
- gelb markierte Bits sind falsch bestimmte (gerade) Paritätsbits
Um den inkorrekten Bit zu finden muss man die **Stellen der falschen bestimmten Kontrollstellen** (Paritätsbits) addieren
- also: $2 + 4=6$ (also 6. Bit muss man invertieren)

## 08.2 Speicher
### 08.2.1 Speicherzellen
![[Pasted image 20250610130800.png]]


### 08.2.2 Blockschema DRAM
Große Empfehlung für das o.g. You-Tube-Video: [Dynamic Random Access Memory (DRAM). Part 2: Read and Write Cycles](https://www.youtube.com/watch?v=x3jGqOrXXc8)   
Hier wird die Funktionsweise des DRAM graphisch erklärt, sowie auch auf die Steuersignale CAS und RAS eingegangen wird.

Der Zugriff auf eine bestimme Zelle der DRAMs erfolgt über eine Adresse, bestehend aus Adressinformationen bezüglich der Zeile und Spalte der Zelle, welche aufeinanderfolgend (unterscheidbar durch die Steuersignale RAS und CAS) übertragen werden. Damit die Zuordnung der Informationen zum richtigen Zeitpunkt und vor allem zum richtigen Zelle erfolgt, benötigen wir den **Control & Timing-Steuerblock.**

Der Prozessor sendet zuerst die Row Address, welche im **Row Address Buffer** gepuffert wird. Der **Row Address Decoder** dekodiert sie und wählt die richtige Zeile aus dem **Memory Array**. Anschließend wird die ausgewählte Wordline aus dem Memory Array in einen Puffer-Speicher (Block unter dem Memory Array) geladen. Der Leseprozess sorgt dafür, dass unsere Kondensatoren ihre Ladung verlieren. Wir müssen also am Ende die gesamte Zeile des Memory Arrays neu laden.

Der Prozessor sendet nun die Column Address, welche im **Column Address Buffer** gepuffert wird. Der **Column Address Decoder** dekodiert sie und wählt die richtige Zelle. Je nachdem, können wir entweder den Inhalt unserer Zelle in den Data Buffer schreiben (Read-Operation), oder wir schreiben den Inhalt unseres Data Buffers, anstelle des dort vorhanden Bits, in den Puffer-Speicher.

Wie Oben erwähnt müssen bevor ein erneuter Zugriff erfolgen kann, die Kondensatoren, der gesamten Zeile, des Memory Arrays neu geladen werden.

![[Pasted image 20250706160934.png]]

### 08.2.3 Innovationen bei Arbeitsspeicher
![[Pasted image 20250610131547.png]]

### 08.2.4 Prefetching in verschiedenen RAM-Generationen
![[Pasted image 20250706161132.png]]
### 08.2.5 Speicherbandbreite 1
*Die Speicherbandbreite eines Systems ist eine prominente Kenngröße. Für gewöhnlich wird derzeit DDR4-Speicher verwendet, **welcher zwei Daten pro Takt** überträgt. In einer Bezeichnung wie "DDR4-3733" ist 3733 die Transferrate in MT/s, nicht der Takt in MHz.*
- Frequenz der Datenbus : 
$$\frac{3733 \cdot 10^{6}\frac{\text{Transfer}}{\text{Sekunde}}}{2 \frac{\text{ Transfer}}{\text{Cycle}}} = 1866.5\ MHz$$
- Intels Xeon Gold 6154 unterstützt DDR4-2666 mit 6 Speicherkanäle auf einer CPU. Wie hoch ist die theoretisch maximale Speicherbandbreite?
	- $DDR\cdot Bustakt$:  Ist die in der Aufgabe gegebene Datenrate : 2666𝑀𝑇/𝑠
	- **Busbreite:** Standartmäßig hat ein DDR4-Speicher eine Busbreite von 64𝐵𝑖𝑡 (8𝐵𝑦𝑡𝑒)
	- **Anzahl Speichercontroller:** Ebenfalls in der Aufgabe gegeben (6 Speichercontroller)

$$
2666 \cdot 10^{6} \frac{\text{T}}{s} \cdot 8 \text{ Byte} \cdot 6 \text{ Speichercontroller}  = 128 \frac{\text{GB}}{s}
$$


### 08.2.6 Speicherbandbreite 2
Ein System mit einem Single-Core-Prozessor, der auf 2.2 GHz taktet und pro Zyklus 4 Befehle abarbeitet, sei mit Dual-Channel DDR4-3200 (auch als PC4-25600 bezeichnet) ausgestattet. Im Mittel soll jede vierte Instruktion 8 Byte aus dem Speicher beziehen. Berechnen Sie die zur Verfügung stehende und die benötigte Bandbreite und prüfen Sie so, ob der Speicher zum Flaschenhals wird.

- **Verfügbare Bandbreite**
	- $DDR\cdot Bustakt$:  Ist die in der Aufgabe gegebene Datenrate : 3200𝑀𝑇/𝑠
	- **Busbreite:** Standartmäßig hat ein DDR4-Speicher eine Busbreite von 64𝐵𝑖𝑡 (8𝐵𝑦𝑡𝑒)
	- **Anzahl Speichercontroller:** Zwar haben wir keine Informationen zur Anzahl der Speichercontroler in unserem System (weswegen wir von einem ausgehen), jedoch haben wir **2 Channels**. Channels sind die physischen Verbindungen zwischen Speichercontroler und Speicher und können gegebenenfalls unsere Verfügbare Bandbreite vergrößern, da durch pro Transfer pro Channel jeweils 8 Byte übertragen werden können.

$$
3200 \cdot 10 ^{6} \frac{\text{T}}{s} \cdot 8 \text{ Byte} \cdot 2 \text{ Channels}=51.2GB
$$

- **Benötigte Bandbreite (single core)**
	- Um die benötigte Bandbreite zu berechnen, müssen wir herausfinden wie viele Befele pro Takt ausgeführt werden, sowie deren Größe bestimmen. Im Falle unseres Single-Core-Prozessors können wir **pro Takt 4 Befehle** abarbeiten, im Schnitt muss jedoch nur **jede 4. Instruktion 8 Byte** aus dem Speicher laden. D.h. das wir jeden Takt 8 Byte aus dem Speicher ziehen müssen.
$$
2.2\text{GB} \cdot 8 \frac{\text{ Byte}}{\text{Takt}}=17.6 \text{ GB}
$$

**Benötigte Bandbreite (4-Kern)**
$$
2.2\text{GB} \cdot 8 \frac{\text{ Byte}}{\text{Takt}} \cdot 4 \text{ Kerne}=70.4 \text{ GB}
$$


## 08.3 Busse
### 08.3.2 PCI Express
#### Symbolrate
$\text{𝑆𝑦𝑚𝑏𝑜𝑙𝑟𝑎𝑡𝑒}=\text{𝑆𝑐ℎ𝑟𝑖𝑡𝑡𝑔𝑒𝑠𝑐ℎ𝑤𝑖𝑛𝑑𝑖𝑔𝑘𝑒𝑖𝑡} \cdot \text{𝐴𝑛𝑧𝑎ℎ𝑙𝐿𝑎𝑛𝑒𝑠} \cdot \frac{1}{8}$
- PCIe 2.0 x16 : $5 \frac{\text{GT}}{s} \cdot 16 \text{ Lanes} \cdot \frac{1}{8}=10 \frac{\text{ GB}}{s}$
- PCIe 4.0 x4 : $16 \frac{\text{GT}}{s} \cdot 4 \text{ Lanes} \cdot \frac{1}{8}=8 \frac{\text{ GB}}{s}$

#### Datenrate 
$𝐷𝑎𝑡𝑒𝑛𝑟𝑎𝑡𝑒=𝑆𝑦𝑚𝑏𝑜𝑙𝑟𝑎𝑡𝑒∗𝑉𝑒𝑟ℎä𝑙𝑡𝑛𝑖𝑠𝐿𝑒𝑖𝑡𝑢𝑛𝑔𝑠𝑐𝑜𝑑𝑒$
- PCIe 2.0 x16 : $10 \frac{\text{GB}}{s} \cdot \frac{8}{10} =8\frac{\text{GB}}{s}$ 
	- da es die 8b/10b Kodierung benutzt 
- PCIe 4.0 x4 : $8 \frac{\text{GB}}{s} \cdot \frac{128}{130} =7.8\frac{\text{GB}}{s}$

### 08.3.3 SMBUs / I2C

Zwischen das *S* und *A* steht die Adresse des Sensors in Bin. -> Umformung in Hex
- S0*110001*1A10000110NP
	- Sensor : 0x31
	- Temperatur: $100001.10 = 33.5 \text{ Kelvin}$
- S01100101A01111000NP
	- Sensor : 0x32
	- Temperatur: $0111100.00 = 30 \text{ Kelvin}$
- S01100111A01101000NP  
	- Sensor : 0x33
	- Temperatur: $011010.00 = 26\text{ Kelvin}$
- S10000010A11000000AP  
	- Aktor: 0x41
	- Befehl: 0xCO
- S10000100A11111111AP  
	- Aktor: 0x42
	- Befehl: 0xFF
- S10000110A00000000AP
	- Aktor: 0x43
	- Befehl: 0x00

**Sensor 0x33|Rd|A|29,5|**
- Um von K in $C^{\circ}$ zu kommen, berechnet man hier $K-10$
S01100111A01110110NP

**Aktor 0x42|WR|A|0xC0**
S1000010A11000000AP

![[Pasted image 20250618172150.png]]


## Encoding
### 8.4.1 NRZ + NRZI Codierung
[[Non Return To Zero]]
Welche Signale müssen Sie mit einer **NRZ**-Kodierung senden, wenn Sie 0x42de übertragen wollen? (Nutzen Sie 1 für ein high-Signal und 0 für ein low-Signal)
- 0100001011011110

Welche Signale müssen Sie für **NRZI** übertragen? (Nutzen Sie 1 für ein high-Signal und 0 für ein low-Signal)
- 0111110010010100
- 0111110010010100