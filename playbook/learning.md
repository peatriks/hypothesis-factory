# Playbook: lernender Teil

> Änderungen nur per Pull Request aus einer Retro. Jede Änderung nennt die Evidenz
> (Experiment-ID oder Quelle) und die Version wird hochgezählt.

**Version:** 0.1 (Ausgangsstand aus Evidenzprüfung 26.09.2026, noch ohne eigene Testdaten)

## Scoring-Gewichte für Hypothesen

| Kriterium | Gewicht | Begründung v0.1 |
|---|---|---|
| Problemintensität | 20 % | |
| Preisplausibilität | 20 % | Kernrisiko laut Evidenzprüfung |
| Lernwert | 15 % | |
| Differenzierung | 15 % | |
| Erreichbarkeit | 15 % | |
| Produktionskomplexität (invertiert) | 10 % | |
| Testkosten | 5 % | |

Kalibrierung: Nach jedem Test wird geprüft, ob der Score-Rang den Ergebnis-Rang vorhergesagt hat.
Liegt er daneben, schlägt die Retro neue Gewichte vor.

## Entscheidungsschwellen

Noch nicht kalibriert. Werden vor dem ersten Test von Patrick in der Experiment-Datei gesetzt
und nach jedem Zyklus hier als Erfahrungswert ergänzt.

| Signal | KEEP | ITERATE | KILL |
|---|---|---|---|
| Reservierungen / 100 qualifizierte Views | offen | offen | offen |
| Kosten pro Landingpage-View | offen | offen | offen |

## Creative- und Seiten-Winkel

| Winkel | Getestet in | Ergebnis |
|---|---|---|
| Schmerz: Verderb, Geld weggeworfen | – | – |
| Genuss: Käse wie vom Affineur | – | – |
| Ordnung/Ästhetik | – | – |

## Freigegebene Formulierungen

- "Konzept: Wir entwickeln gerade ..."
- "Geplanter Preis: XX €. Noch nicht erhältlich. Trag dich ein, wir melden uns zum Start."
- "Visualisierung (KI-generiert), finales Produkt kann abweichen"
- "Frühe Unterstützer erhalten Vorabzugang"

## Prüfliste vor Live-Schaltung

- [ ] Konzeptstatus, Preis, Visualisierungshinweis sichtbar
- [ ] Pixel feuern erst nach Einwilligung
- [ ] Double Opt-in funktioniert
- [ ] Anzeige und Landingpage inhaltlich deckungsgleich
- [ ] Lifetime-Budget und Kontolimit gesetzt
- [ ] Vorab-Festlegung committet
- [ ] Impressum (§ 5 DDG) und Datenschutzerklärung passend zu den tatsächlichen Datenflüssen
- [ ] Kampagnenstatus und Zeitplan explizit gesetzt (Pinterest-API kann sonst sofort aktivieren)
