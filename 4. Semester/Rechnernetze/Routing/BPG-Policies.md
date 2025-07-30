## Beziehungen
- Kunde - Provider 
	- Kunde bezahlt den Provider 
- Peer to Peer 
	- Bezahlen sich gegenseitig nicht 
	- Peers stellen keinen Transit für anderen Peers bereit (nur Providers)

## Export Regeln 
|          | Kunden | Peer | Provider |
| -------- | ------ | ---- | -------- |
| Kunden   | ja     | ja   | ja       |
| Peer     | ja     | -    | -        |
| Provider | ja     | -    | -        |
- Kunden annoncieren IP-Präfixe an andere Kunden, Peers und Providers 
- Peers annoncieren IP-Präfixe nur an Kunde
