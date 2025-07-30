Here are the steps of the algorithm:

Apply a threshold to the 2D field to make a [binary](https://en.wikipedia.org/wiki/Binary_numeral_system "Binary numeral system") image containing:

- 1 where the data value is _above_ the isovalue
- 0 where the data value is _below_ the isovalue

Note: Data equal to the isovalue has to be treated as _above_ or _below_ in a consistent way.

Every 2x2 block of pixels in the binary image forms a contouring cell, so the whole image is represented by a grid of such cells (shown in green in the picture below). Note that this contouring grid is one cell smaller in each direction than the original 2D field.

For each cell in the contouring grid:

1. Compose the 4 [bits](https://en.wikipedia.org/wiki/Bit "Bit") at the corners of the cell to build a binary index: walk around the cell in a [clockwise](https://en.wikipedia.org/wiki/Clockwise "Clockwise") direction appending the [bit](https://en.wikipedia.org/wiki/Bit "Bit") to the index, using [bitwise OR](https://en.wikipedia.org/wiki/Bitwise_OR "Bitwise OR") and [left-shift](https://en.wikipedia.org/wiki/Logical_shift "Logical shift"), from [most significant bit](https://en.wikipedia.org/wiki/Most_significant_bit "Most significant bit") at the top left, to [least significant bit](https://en.wikipedia.org/wiki/Least_significant_bit "Least significant bit") at the bottom left. The resulting 4-bit index can have 16 possible values in the range 0–15.
2. Use the cell index to access a pre-built [lookup table](https://en.wikipedia.org/wiki/Lookup_table "Lookup table") with 16 entries listing the edges needed to represent the cell (shown in the lower right part of the picture below).
3. Apply [linear interpolation](https://en.wikipedia.org/wiki/Linear_interpolation "Linear interpolation") between the original field data values to find the exact position of the contour line along the edges of the cell.

#### The Iso-value is given in the exercise

![[Screenshot from 2024-05-07 14-01-29.png]]

## Ambiguous cases 
- Case 5 and Case 10 can be mixed 
![[Screenshot from 2024-05-07 14-17-07.png]]

=> Dann muss man den Mittelwert bestimmen
- 4 (Eck) Werte addieren und durch 4 teilen

###### 1. Fall => Mittelwert kleiner als Iso-Wert:
- Dann werden die Tale miteinander verbunden

###### 2. Fall => Mittelwert grosser als Iso-Wert:
- Dann werden die Berge miteinander verbunden![[WhatsApp Image 2024-05-07 at 14.22.46.jpeg]]