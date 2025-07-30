## Domain Name System
- Auflösung von Namen zu (z.B.) IP-Adressen, damit ein Gerät das Server im Internet finden kann 


### Schritte 
1. **Client Anfrage**
	1. Client sendet eine DNS-Abfrage zu den konfigurierten DNS-Resolver
2. **Püfung des Lokalen Caches**
	1. Der DNS-Resolver überprüft zunächst seinen Cache, ob die *IP-Adresse für den angefragten Domainnamen bereits bekannt ist* und **noch gültig** ist (basierend auf der TTL, Time-to-Live)
	2. Falls die Information im Cache vorhanden ist, wird die **IP-Adresse direkt an den Client zurückgegeben**, und der Prozess endet hier
3. **Rekursive Abfrage an den Root Server**
	1. Der Resolver sendet eine Anfrage für den Domainnamen zu den Root Server
	2. Der Root-Nameserver antwortet mit einer Referenz zu den zuständigen TLD-Nameservern für die Top-Level-Domain
	3. Die Root-Nameserver kennen die Adressen der **Top-Level-Domain** (TLD)-Nameserver (**z. B. für .com, .org, .de**).
4. **Anfrage an den TLD-Nameserver**
	1. Der Resolver kontaktiert den zuständigen TLD-Nameserver (z. B. den *Nameserver für .com*, betrieben von Verisign)
	2. Der TLD-Nameserver kennt die autoritiven Nameserver für die Second-Level-Domain (z. B. **example**.com)
5. **Abfrage an den Autoritativen Nameserver**
	1. Der Resolver fragt nach dem spezifischen Hostnamen (z. B. www.example.com)
	2. Der autoritative Nameserver antwortet mit dem entsprechenden **DNS-Eintrag**
6. **Antwort an den Client** 
	1. IP-Adresse an den Client weitergegeben 
	2. Resolver Speichert Antwort im Cache 

### Iterative und Rekursive Anfragen 
- Der Resolver führt *rekursive Abfragen im Auftrag des Clients* durch, d. h., er übernimmt die gesamte Arbeit der Auflösung
- Zwischen **Resolver und Nameservern** (Root, TLD, autoritativ) werden *iterative Abfragen verwendet*, bei denen jeder Nameserver nur den nächsten Schritt angibt