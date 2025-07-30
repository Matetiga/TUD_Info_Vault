## Formel
mit : 
- **B** : Brandbreite in $Hz$
- **b** : Bitrate in $\frac{Bit}{s}$
- **S**: Signalstufen 
- **SNR** : Signal-Rauschabstand
	- $SNR = \frac{\text{ Signalleistung}}{\text{ Rauschleistung}}$
	- $SNR_{dB} = 10 \cdot lg(SNR)$ 

### Nach Nyquist 
$$
b < 2 \cdot B \cdot ld(S)
$$
### Nach Schannon
$$
b < B \cdot ld(1 + \text{ SNR})
$$
### Kommbiniert 
$$
b < min(2 \cdot B \cdot ld(S); B \cdot ld(1 + \text{ SNR}))
$$