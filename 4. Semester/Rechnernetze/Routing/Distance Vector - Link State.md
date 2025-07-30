## Distance Vector
Jeder Router tauscht mit seinen Nachbarn eine Liste ihm aller bekannten Ziele und die damit verbundenen Kosten aus

Knoten geben nur Ziel und Distanzen zu Zielen bekannt
- Weniger Komplex 
- Weniger Ressourcen 
- *Weniger Stabil*
### Beispiel 
- RIP (*Routing Information Base*) Protokoll

---


## Link State 
Jede Knoten kennt alle Wege (gesamt Topologie des Netzes)
- Stabiler 
- aufwändiger
Shortest Pfad wird mit Hilfe von Disjktra Algorithmus gefunden

### Beispiel 
- OSPF Protokoll