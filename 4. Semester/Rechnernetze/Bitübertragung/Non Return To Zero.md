## NRZ
Eine Methode zur digitalen Signalübertragung, bei der die Signalpegel während eines Bitintervalls konstant bleiben und nicht auf einen Nullpegel zurückkehre
- **Übergänge**: Ein *Pegelwechsel erfolgt nur*, wenn sich der Bitwert zwischen zwei aufeinanderfolgenden Bits ändert (z. B. von 1 zu 0 oder umgekehrt
- **Kein Rückkehr zu Null:** Im Gegensatz zu anderen Verfahren wie RZ (Return-to-Zero) bleibt der Pegel während des gesamten Bitintervalls unverändert, ohne zwischendurch auf einen



## NRZI
**Der Signalpegel ändert sich nur** , wenn **ein Bit eine 1 ist**, und bleibt gleich, wenn es eine 0 ist. Dies wird oft in differentiellen Kodierungen verwendet
-  *Signalpegel  toggle*

###  Beispiel
- Bit 1: **1** → Pegel toggelt → **hoch (1)**.
- Bit 2: **0** → Pegel bleibt → **hoch (1)**.
- Bit 3: **1** → Pegel toggelt → **niedrig (0)**.
- Bit 4: **1** → Pegel toggelt → **hoch (1)**.
- Bit 5: **0** → Pegel bleibt → **hoch (1)**.
- Bit 6: **0** → Pegel bleibt → **hoch (1)**