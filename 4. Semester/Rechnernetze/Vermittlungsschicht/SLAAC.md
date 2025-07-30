## Stateless Address Autoconfiguration
Geräte generieren automatisch Adressen basierend auf Router-Advertisements 

### Schritte 
*Interface* ist diee Netzwerkschnittstelle des Geräts (Host), für die die Kommunikation im Netz zuständig ist 
1. Host erzeugt (bei Aktivierung) für *Interface* eine [[Link Local IPv6]] Adresse (z.B. aus der Hardwareadresse).
2. Zur Verifikation der Eindeutigkeit wird noch eine [[ICMP]] Neighbor Solicitation versandt (Duplicate Address Detection, DAD).
3. Interface sendet **Router Solicitation**, um nicht auf Router Advertisements warten zu müssen.
4. Router sendet Router Advertisement (*Präfix, Default Gateway,* …).
5. Das Interface bildet aus Präfix und link-lokaler Adresse eine **globale Adresse**. Prüfung der Eindeutigkeit mittels DAD

---

## Unterschiede zwischen [[SLAAC]] und [[DHCP]]
### SLAAC
- wird für [[IPv6]] verwendet
- selbständige Konfiguration 
- Adresse ist abhängig von MAC-Adresse (durch [[Link Local IPv6]] Addresse)
- falls autogenerierte Adresse bereits vergeben,  manuelle Konfiguration des Interface notwendig
- liefert *IP-Adress und Standard-Gateway*
- Ein IPv6 Rechner braucht zwei IPv6 Adressen
	- [[Link Local IPv6]] zur Kommunikation innerhalb des (lokalen) Netzwerk
	- Globale Adresse zur Kommunikation ausserhalb des Netzwerkes 

### DCHP
- Vergabe von Adressen kontrolliert und protokolliert 
- Konfiguration Zusätzliche Netzwerkdienste (*DNS-Server, Default Gateway, NTP*)
- DCHPv6 wird nicht von alle Geräte unterstützt (z.B.: Android)

### Simultäne Nutzung 
Man kann beide Services nutzen, wenn man: 
- Geräte mit einer IPv6 Adresse versorgen will und extra Konfigurationsdaten (DNS, NTP, Default-Gateway)