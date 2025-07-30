- Dient zur Verbesserung der Bildqualität
- Funktioniert durch Erhöhung des Abstastrate
	- mehr Pixel werden Berechnet als die letztlich gezeigt werden 
- 

## Vermeidung Treppenstufenartefakten (Aliasing)
- Aliasing tritt auf, wenn zu wenige Abstastpunkte verwendet werden, **um eine feine Struktur oder scharfe Kante darzustellen**

Supersampling erhöht der Abtastrate, was die Kanten glätten wird


### Supersampling Strategie
- Bild wird in einer höheren Auflösung berechnet und dann Auflösung mit Filtern reduziert
- pro Pixel wird Supersampling durchgeführt je nach Anordnung

#### Anordnungen
- Gitter
	- Regelmäßig verteilte Punkten

- Zufallspunkten
	- Zufällige verteilte Punkten 
	- können sich auf einer Stelle grupieren
- Poisson Disk Sampling
	- Zufällige verteilte Punkten haben ein minimal Abstand zueinader, was Hilft, **dass Punkten nicht NUR auf einer Stelle sind** => <span style="color:#ffff00">Regelmäßig verteilt</span>
- Jitter
	- Zufällig in Zellen einer regulären Unterteilung