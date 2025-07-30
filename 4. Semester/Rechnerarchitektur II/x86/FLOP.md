Floating Operation per Takt 
$$
\frac{\text{Instructions}}{\text{cicle}} \cdot \frac{\text{vector length}}{\text{operand length}} \cdot \frac{\text{Operations}}{\text{Instruction}} \cdot \text{Frequenz} = \text{ FLOP }
$$


### Beispiel 
*2 SIMD Einheiten (AVX – wird nativ 256b-breit ausgeführt, FMA), double precision, 2.5 GHz*
- 2 SIMD Einheiten : $2 \frac{\text{Instructions}}{\text{cicle}}$
- AVX : $\frac{256\text{ vector length}}{64\text{ operand length}}=4$
- FMA : $2\frac{\text{Operations}}{\text{Instruction}}$
- Frequenz : $2.5 \cdot 10^{9} \ Hz$
$$2 \frac{\text{Instructions}}{\text{cicle}} \cdot 4 \cdot 2\frac{\text{Operations}}{\text{Instruction}} \cdot 2.5 \cdot 10^{9} Hz=40 \text{ GFLOP}$$
