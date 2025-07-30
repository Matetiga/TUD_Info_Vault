## Flat 
Sehr einfaches Schattierungsmodel
- Jedes Pixel innerhalb eines Polygons erhält **dieselbe Farbe** 
- eckig formig 
- nur ein Flächennormale pro Polygon

---

## Gouraud
Zerluegung gekrummte Flächen in Polygone
- Einselne schattierung der Polygone mit ihrer Normalenvektor
- jeden Eckpunkt hat sein eigenen Normalenvektor 
- Mehr Realitätstreu als Flat-Schattierungsmodell


--- 

## Phong
(Phong Schattierungsmodell ist nicht dasselbe als Phong Beleuchtungsmodell)
- Per Pixel Verfahren \
- Beleuchtung wird für jedes Pixel berechnet
- 