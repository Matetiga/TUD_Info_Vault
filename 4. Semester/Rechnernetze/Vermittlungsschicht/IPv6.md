## Eigenschaften
- besteht aus 8 16-Bit Hexadezimal Zahlen ($2^{128}$)
- Aufeinander folge von 0000 Blocke werden durch "::" ersetzt
	- *2001:0DB8:0000:0000:0000:0000:0000:1*
	- **2001:0DB8::1**

![[Pasted image 20250607210814.png]]

## Neue Adressfunktionen
IPv6 hat neue Adressfunktionen im Vergleich mit IPv4, da die Struktur anders ist 
- Neue Adresslänge und darstellung 
### Neue Adresstypen und -bereiche
- *Unique Local* : 1111 110 -> FC00::/7
- *link-local* : 1111 1110 10 -> FE80::/10
- *IPv4-Mapped* : 000…0:FFFF -> ::FFFF:0.0.0.0/96
- *Loopback* : 0000..1 -> ::1/128
- *unspecified* : 0000…0 -> ::/128

### Autokonfiguration 
- IPv6 nutzt [[SLAAC]], Dies führt oft dazu, dass eine Netzwerkschnittstelle mehrere Adressen (z. B. Link-Local und Global) gleichzeitig hat

---



