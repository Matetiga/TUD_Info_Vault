- Pro Pixel werden **mehrere Strahlen verfolgt** (nicht nut eine wie im nomalen Raytracing)
- Simulation von Effekte
	- *Unschärfeffekte* 
		- **Depth of Field** (Tiefenschärfe)
			- Position auf der Linse
		- **Motion Blur** (Bewegunsunschärfe)
			- Zeitpunkt

	- *weichere Schatten simulieren*
		- Position auf Flächelichtquelle

	- *difusse Spiegelung*
		- Reflektionswinkel

	- *Anti-Aliasing*
		- Subpixelposition


### Erzeugung weichere Schatten (Soft Shadows)
Strahlen werden über die Lichtquelle verteilt (**Bei einer Flächenlichtquelle**)
- Licht trifft von verschiedene Punkten auf die Szene
- pro Sample werden Strahlen zu zufällig gewählte Punkten auf der Flächenlichtquelle geschickt 
