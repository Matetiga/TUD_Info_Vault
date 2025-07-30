The IP is applied a *AND bitwise Operation* with the Mask, so can you get the routing prefix
- 198.51.100.20/24 has the subnet mask 255.255.255.0
- **Network prefix** : 198.51.100.0
- **Host prefix** : 0.0.0.20


## Beziehung mit Host anzahl
die Network-Maske zeigt die Anzahl an mögliche Hosts, die ein Netz haben kann 
- Maske: 255.255.224.0 bzw. 1111 1111 . 1111 1111 . 111<mark style="background: #BBFABBA6;">0 0000 . 0000 0000</mark>
	- also es gibt $2^{13}-2$ mögliche Hosts
	- da man eine *Addresse für die Netzaddresse und  Broadcast-Addresse* braucht
	- die **erste Addresse** ist immer die Netzaddresse 
	- die **letzte Addresse** ist immer die Broadcast-Addresse
