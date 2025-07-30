## Aufbau
- **Rahmenbegrenzer**: 0111 1110
- **Addresse** : meist auf 1111 1111
- **Steuerung** (Sequenz des Frames)
- **Protokoll** (z.B. für IP: 0x0021 )
- **Nutzdaten**
- **CRC-Prüfsumme**
- **Rahmenbegrenzer**  : 0111 1110

### Beispiel 
zu Übermittlung des Worts "Token"
- T  : 101 0100
- o : 110 1111
- k : 110 1011
- e : 110 0101
- n : 110 1110
**0111 1110**  101 0100 11*0 1111 110* 1011 110 0101 110 1110 **0111 1110**
- Es entsteht ein mögliches Fehler bei der Kodierung zwei Buchstaben 

#### Korrektur 
Falls fünf "1" nacheinander gefunden werden, wird das sechste Bit zu 0 umgewandelt 
- Der Empfänger muss dann dieses Bit wieder auf 1 stellen
- **0111 1110**  101 0100 11*0 1111 1**0**0* 1011 110 0101 110 1110 **0111 1110**