## Address Resolution Protocol 
### MAC-Address aus IP-Address (IPv4) 
Für den Prozess wird das [[Schichtenmodell#2. Data Link|Link-Schicht]] genutzt
1. Sender sendet eine ARP-Anforderung (ARP  Request) inkl. der gesuchten IP-Adresse an  Broadcast-Adresse (*ff:ff:ff:ff:ff:ff*)
2. Host mit angefragter IP-Adresse hat sich gemeldet  und seine MAC-Adresse in ARP-Antwort (ARP Reply)  zurückgesendet (alternativ: keine Antwort→ Timeout)
3.  Information wird **ARP-Tabelle** (ARP Cache)  vorübergehend gespeichert, sodass künftige  Anfragen schneller beantwortet werden können

### Für IPv6
Der Prozess wird in Layer 3 gemacht ([[Schichtenmodell#3. Network|Network Layer]])
- dafür wird ein Multicast genutzt 


