### Ansatz mit Grenzwert
- beim Aufladen geht $u_{c,t \to \infty} \to U_{b}$
- beim Entladen geht $u_{c,t \to \infty} \to 0 V$
(tgiFormel::$$u_{c}(t)=u_{c, t \to \infty}+ [u_{c, t_{0}}-u_{c, t \to \infty}] \cdot e^{-t/\tau}$$)

## Aufladenverhalten 
- mit : $U_{q}=u_{R}(t_{0})$
(tgiFormel::$$u_R(t) = U_{q}\left( 1 - \exp \left(-\frac{t - t_0}{\tau}\right) \right)$$)
(tgiFormel::$$i_{C}(t)=i_R(t) = I_0 \cdot \exp\left(-\frac{t - t_0}{\tau}\right), \quad I_0 = \frac{U_0}{R}$$)

## Entladenverhalten 
- mit : $U_{q}=u_{R}(t_{0})$
(tgiFormel::$$u_R(t) = U_{q} \exp \left(-\frac{t - t_0}{\tau} \right)$$)
(tgiFormel::$$i_{C}(t)=i_R(t) = -I_0 \cdot \exp\left(-\frac{t - t_0}{\tau}\right), \quad I_0 = \frac{U_0}{R}$$)
- Negatives $I_{0}$, da es in der **entgegengesetzte Richtung** fliesst
![[Screenshot from 2024-11-27 13-20-13.png]]![[Screenshot from 2024-11-27 13-20-18.png]]