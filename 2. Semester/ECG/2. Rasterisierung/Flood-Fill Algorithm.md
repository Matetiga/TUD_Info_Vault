## Pseudocode
### 4er Nachbarschaft
void floodFill(x,y)
	if not toBeFilled(x, y) return
	setPixel(x, y, drawColor)
	floodFill(x+1, y)
	floodFill(x-1, y)
	floodFill(x, y+1)
	floodFill(x, y-1

---

### 8er Nachbarschaft
void floodFill(x,y)
	if not toBeFilled(x, y) return
	setPixel(x, y, drawColor)
	floodFill(x+1, y)
	floodFill(x-1, y)
	floodFill(x, y+1)
	floodFill(x, y-1)
	floodFill(x+1, y+1)
	floodFill(x-1, y+1)
	floodFill(x+1, y-1)
	floodFill(x-1, y-1)
	
---

### toBeFilled() checks if:
- Pixelposition is valid
- FloodfFill had previously overwritten the pixel
- Pixel-Farbe der Farbe des Saat-Pixel ähnelt


# Problem:
This algorithm can cause Stackoverflow for too big areas
- this can be avoided by changing the recursion deepness

