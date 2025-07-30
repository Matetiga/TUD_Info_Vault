Ein Port kann sowohl *tagged* als auch *untagged* konfiguriert werden 
-  Aber es kann nur für eine [[VLAN]] als **untagged** sein 
- Für alle anderen müssen die Tags vorhanden sein 
---
## Untagged 
- Alle Packete die zu diesem Port *reinkommen*, werden **ein VLAN-Tag und VLAN-ID** eingefügt
- Alle Packete die diesen Port *verlassen* werden das **VLAN-Tag und VLAN-ID entfernt** 
- Diese Optopn kann **nur auf ein einziges VLAN Port** konfiguriert werden

## Tagged
Packete werden nur akzeptiert oder weitergeleitet falls:
- Packet ein VLAN-Tag mit VLAN-ID des VLANs besitzen
- VLAN-Tags und VLAN-IDs werden nicht hinzugefügt noch entfernt 
---
