## Wird benutzt, um Fehler in empfangene Kodewörter zu finden


Die **Empfangsworte** $b^{T}$ kann als Überlägerung eines **Kanalwortes** $a$ und einem **Fehlerwort** $e$ aufgefasst werden
### $b=a_{i} \oplus e$

### $s = H_{k \times n} \cdot b^{T}=0(\text{ Nullvektor})?$
- falls $= 0$, dann gibt es **keinen Fehler** (*oder würde nicht erkennt*)
- falls $\not =0$, dann gibt es einen **Fehler**

#### Falls ein Fehler erkannt würde, ist dieses Vektor gleich <span style="color:#ffffff">wie eine Spalte</span> in der Kontrollmatrix
- somit korrigiert man dieselbe Spalte im empfangenen Kodewort

---
### Fehler mit Sicherheit Korrigierbar
$$
w(e)\leq \lfloor \frac{d_{min}-1}{2} \rfloor 
$$
