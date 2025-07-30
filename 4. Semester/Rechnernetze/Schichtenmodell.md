Jedes Schicht nutzt die Dienste, gegeben direkt vom unteren Schicht 
## Modell 
![[Pasted image 20250420111335.png]]
### 1. Bitübertragungsschicht
Umsetzung in elektrische Signale (z.B. „0“=1V); mechanische und elektrische Kopplung (z.B. RJ45-Stecker)
### 2. Data Link
Rahmenbildung; Behandlung von Übertragungsfehlern (Prüfsummen, Wiederholung) *Überlastvermeidung* (Flusssteuerung)
### 3. Network
- Weiterleitung von [[Frame - Packet#Packet|Packeten]]
 Wegewahl Sender → Empfänger (statisch oder dynamisch); Kopplung heterogener Teilnetze (Anpassung, Abrechnung)
### 4. Transportschicht
Sichere Ende-zu-Ende-Kommunikation zwischen Prozessen; Multiplex, Bündelung, Flusssteuerung zwischen Endsystemen
### 5. Sitzungsschicht
(*Kommunikationssteuerung*): Dialogsteuerung (simplex/duplex/halbduplex); Synchronisation (Sicherungspunkte, Transaktionen)
### 6. Darstellungsschicht
Transformation zwischen Datenformaten (z.B. ASCII/EBCDIC); Kompression (z.B. MPEG, MP3), **Verschlüsselung** (z.B. *RSA*)
### 7. Anwendungsschicht
Kommunikation zw. Anwendungen, spezielle Dienste (z.B. RPC, FTP, E-Mail, Telnet, WWW)

