## Definition

Ein **polynomieller Verifikator** für eine Sprache $L ⊆ Σ^{*}$ ist eine polynomiell-
zeitbeschränkte, deterministische TM $M$, für die gilt:
• $M$ akzeptiert nur Wörter der Form $w\#z$ mit:
-  w ∈ L,
- $z ∈ Σ^{*}$ ist ein **Zertifikat** *polynomieller Länge*
	(d.h. für $M$ gibt es ein Polynom $p$ mit $|z| ≤ p(|w|))$

• Für jedes Wort $w ∈ L$ gibt es ein solches Wort $w \#  z  \in L(M)$

### Intuition
Das Zertifikat z kodiert die Lösung der Probleminstanz w, die der Verifikator
lediglich nachprüft.
- Die Prüfung selbst (Verifikator prüfen) sollte nicht länger als die Lösung des Problems sein

---

## Zertifikat
Ist was prüft, dass etwas in der Klasse liegt (also erfüllbar ist)
- Ein Zertifikat **trifft keine Entscheidung** bei der Prüfung, dass eine Formel **nicht erfüllbar ist** 

"You do not rise to the level of your goals. You fall to the level of your systems." by James Clear ^quote-of-the-day

