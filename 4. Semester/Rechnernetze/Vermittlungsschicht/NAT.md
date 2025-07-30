## Network Address Translation
Dient zur übersetzung einer privaten IP in einem offentlichen IP
- Mehrere Geräten können dasselbe offentliche IP-Adresse nutzen um in die Internet zugreifen

### Static  NAT
feste Zuordnung,
- z. B. 192.168.54.3 → 214.15.23.1

### Dynamic NAT
dynamische Zuordnung der ersten freien globalen IP-Adresse aus einem Adresspool
- Rechner sind dann von außen nicht direkt anrufbar (Problem bei Voice-over-IP etc.

--- 

## Probleme bei NAT
**Prüfsummen von Paketköpfen**
- Änderung der IP-Adresse (oder TCP-Port-Nummern) erforder das Neuberechnen der Prüfsumme 

**Fragmentierung**
- Transport-Ports sind Teil des ersten Fragments. Pakete können außerhalb der Reihenfolge ankommen. Das NAT-Gerät muss Zustände pro Fragement speichern.
 
**Verschlüsselung**
Verschlüsselte Paketköpfe können nicht verändert werden

**Protokoll-spezifische Probleme oberhalb der Netzwerkschicht** 
- Anwendungsprotokolle beinhalten u.U. die IP-Adresse. Schränkt Innovationen auf der Transportschicht ein