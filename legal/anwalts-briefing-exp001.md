# Anwalts-Briefing: Konzepttest EXP-001

**Stand:** 26.09.2026, Entwurf Worker (Backlog K2). Keine Rechtsauskunft, sondern Fragen an die Kanzlei.
**Vor dem Versand füllt Patrick nur die drei `[…]`-Felder aus.**
Grundlage: `playbook/fixed.md`, `research/2026-09-26-claude-evidenzpruefung.md` (Abschnitt 9), `research/2026-09-26-chatgpt-deep-research.md` (Abschnitte 5, 9).

---

## Anschreiben (zum Weiterleiten)

Wir planen einen Online-Konzepttest für Aufbewahrungsbehälter aus Glas, die es **noch nicht gibt**. Deutschland, Endverbraucher.
Anbieter und Verantwortlicher: **[Name/Rechtsform]**. Budget für die Prüfung: **[Betrag oder „bitte Angebot“]**. Gewünschter Termin: **[Datum]**.

**Ablauf:** Social-Media-Anzeige (Meta, Pinterest oder TikTok, Link-Anzeige) → Konzeptseite in einem eigenen Shopify-Store mit Produktbeschreibung, Visualisierung und geplantem Preis → freiwillige Anmeldung per E-Mail mit Double Opt-in → danach drei freiwillige Fragen. **Es gibt keine Bestellung und keine Zahlung.** Eine Reservierung mit Anzahlung ist erst für einen späteren Test geplant (Teil F).

**Wir bitten um:** (1) Freigabe bzw. Korrektur eines Seiten-Templates und der Texte unten, gültig für mehrere Produktvarianten, (2) kurze schriftliche Antworten auf die Fragen, (3) einen Hinweis, was vor Teil F zusätzlich nötig ist.

## A. Konzeptseite und Werbung (UWG, PAngV)

Geplante Pflichtbausteine: Konzeptstatus, Preis inkl. MwSt. „above the fold“, Hinweis auf Visualisierung. Kein „auf Lager“, kein „jetzt kaufen“, keine Lieferzeit, keine Streichpreise, keine Frische- oder Wirkversprechen.

1. Reichen diese Formulierungen, um keinen Eindruck der Verfügbarkeit zu erwecken (§§ 5, 5a UWG)?
   - „Konzept: Wir entwickeln gerade …“
   - „Geplanter Preis: XX €. Noch nicht erhältlich. Trag dich ein, wir melden uns zum Start.“
   - „Dieses Produkt ist noch nicht erhältlich. Wir testen derzeit das Interesse am beschriebenen Konzept. […] Es gibt keine Bestellung und keine Zahlung.“
   - „Frühe Unterstützer erhalten Vorabzugang“
2. Greift die PAngV bei einem reinen Konzept ohne Angebot? Wenn ja: Muss „zzgl. Versand“ oder ein Grundpreis stehen?
3. Ist ein Anhang-Tatbestand zu § 3 Abs. 3 UWG relevant (z. B. Nr. 5, Lockangebote)?
4. Wir zeigen zufällig verschiedenen Besuchern unterschiedliche Preise (z. B. 69 € / 89 €). Ist das zulässig, und muss es offengelegt werden?
5. Muss auch die Anzeige selbst „Konzept / noch nicht erhältlich“ enthalten, oder reicht die Landingpage?

## B. KI-generierte Produktbilder (Art. 50 AI Act)

Die Visualisierungen sind KI-generiert oder KI-bearbeitet. Laut Sekundärquellen gilt Art. 50 seit 02.08.2026; täuschungsgeeignete KI-Produktbilder seien kennzeichnungspflichtig (Leitlinientext von uns nicht geprüft).

6. Ist „Visualisierung (KI-generiert), finales Produkt kann abweichen“ ausreichend? Wo muss der Hinweis stehen: im Bild, in der Anzeige, auf der Seite?
7. Ändert sich etwas, wenn wir ein CAD-Rendering nur mit KI-Hintergrund nutzen?

## C. Anmeldung und Qualifizierungsfragen (UWG § 7, DSGVO)

Geplante Double-Opt-in-Anmeldung für Informationen zum Produktstart. Danach drei freiwillige Freitextfragen: (1) heutige Lösung, (2) letzter Vorfall mit dem Problem, (3) bisher dafür ausgegebenes Geld.

8. Welche Einwilligungstexte brauchen wir, wenn wir trennen zwischen einmaliger Startinfo, Newsletter und Nutzung der Antworten zur Produktentwicklung?
9. Rechtsgrundlage und Pflichtinformationen (Art. 13 DSGVO) für die Qualifizierungsfragen? Ist eine Verknüpfung mit der E-Mail-Adresse zulässig, oder sollten wir anonym auswerten?
10. Welche Speicherdauer und Löschregel empfehlen Sie, wenn das Produkt nie kommt?
11. Dürfen wir den Kontakten später ein Reservierungsangebot (Teil F) schicken?

## D. Tracking und Consent (§ 25 TDDDG, DSGVO)

Ad-Pixel (Meta, Pinterest oder TikTok) feuern erst nach Einwilligung über das Consent-Banner, Ablehnen gleichwertig. Shopify und die Werbeplattform sitzen (teilweise) außerhalb der EU; Rollen und Transfers sind von uns nicht geprüft.

12. Reicht Shopifys Standard-Consent-Lösung, oder brauchen wir eine eigene CMP?
13. Für die Werbeplattformen: gemeinsame Verantwortlichkeit oder Auftragsverarbeitung? Welche Verträge brauchen wir?
14. Muss auch ein serverseitig übermitteltes Conversion-Event (z. B. Conversions API, bestätigter Opt-in) von der Einwilligung abhängen? (Unsere interne Regel: nur nach Einwilligung.)

## E. Impressum und Datenschutzerklärung (§ 5 DDG)

15. Welche Angaben braucht das Impressum für **[Name/Rechtsform]**? Reicht eine ladungsfähige Geschäftsadresse?
16. Können Sie die Datenschutzerklärung für die tatsächlichen Datenflüsse (Shopify, E-Mail-Tool, eine Werbeplattform) prüfen oder erstellen?

## F. Später: Reservierung mit Anzahlung (nicht für EXP-001)

Idee: voll rückerstattbare Anzahlung über den Shopify-Checkout, ohne Liefertermin.

17. Wird damit ein Fernabsatzvertrag geschlossen (Widerruf, Informationspflichten)?
18. Welcher Liefertermin muss genannt werden (Art. 246a § 1 EGBGB)? Laut Sekundärquellen reichen „bald verfügbar“ oder „voraussichtlich“ nicht (LG München I). Wir zitieren die Norm-Nummer uneinheitlich, bitte prüfen.
19. Gibt es eine Konstruktion, bei der eine Anzahlung ohne festen Liefertermin zulässig ist (z. B. Option statt Kauf)?

---

*Bitte rückmelden: freigegeben / mit Änderungen / nicht zulässig. Jeweils pro Frage.*
