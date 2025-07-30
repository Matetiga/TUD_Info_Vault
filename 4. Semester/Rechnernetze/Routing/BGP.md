- BGP-Routern erfahren Wege zu Präfixen von ihren Nachbarn (**BGP-Peers**)

>[!Important]
>Durch BGP tauschen **ASes** IP-Präfixe, die sie erreichen können (*direkt oder indirekt*)
>Falls ein Router ein Präfix nicht exportiert, dann wissen andere ASes nicht über den Präfix (*einkommende Traffik vermeidet*), aber man kann von diesem Präfix andere ASes erreichen (*ausgehende Traffik funktioniert*)

- Ein BGP-Router kennt nur die Pfade die es vom Nachbarn bekommt (**NICHT alle AS-Pfade**)
## Border Gateway Protocol 
BGP is the protocol that allows these routers to exchange and maintain this complete routing information across autonomous systems (ASes)
- Without BGP, the [[DFZ]] could not exist, as BGP **provides the mechanism for advertising, updating, and selecting routes**
- Alle Teilnehmende in einer DFZ (definiert von BGP)  müssen eine vollständige ortsabhähangige verschiedene [[RIB]] (*Routing Information Base*) haben 

 Used to interchange routing and reachability information across ASes (*Autonomous Systems*)
- Each **AS** is identified by its own unique AS Number (*ASN*)
- BGP is used for routing between ASes 
	- Unlike RIP or OSPF that operate within an AS


---

# BGP4
Is the current used version of the Border Gateway Protocol
- Uses CIDR (Classless Inter-Domain Routing) to divide IP ranges into separated networks ([[IP Mask - CIDR]])

---

