# Evidenzprüfung 26.09.2026: Zusammenfassung

> Kurzfassung des vollständigen Berichts "Hypothesen-Test-Factory für eine Premium-Aufbewahrungsmarke".
> Der Volltext sollte als `research/2026-09-26-evidenzpruefung.md` ergänzt werden.

## Urteil

Autonome Factory noch nicht bauen. Zuerst ein manueller Pilot über 4 bis 6 Wochen: H1 (Obst/Gemüse) und H2 (Käse), Meta als erster Paid-Kanal, sichtbarer Preis, Reservierungsstufe als Kaufsignal. Google Search für Konzeptseiten ist das riskanteste Element.

## Kernbefunde

| Thema | Befund | Status |
|---|---|---|
| Nachfrage Obst/Gemüse | 35 % des vermeidbaren Haushaltsabfalls (BMEL/GfK 2020) | Problem bestätigt, Premium ungeklärt |
| Zahlungsbereitschaft 79 bis 169 € | Keine Primärquelle gefunden; DE-Premium heute 50 bis 75 € für Kunststoff-Systemsets, 10 bis 25 € pro Einzelbehälter | Kritischste Annahme |
| Warteliste | Bei physischen Produkten unter 5 % Kaufkonversion (Lenny Rachitsky) | Nur Discovery-Signal |
| Concept-Ads Meta/TikTok/Pinterest | Nicht ausdrücklich verboten, wenn Anzeige und Seite deckungsgleich sind und keine Verfügbarkeit suggeriert wird | Interpretation |
| Shopping/Katalog/Feed | Setzen kaufbares Produkt voraus | Bestätigt |
| Google Search | Misrepresentation-Policy, Sperre ohne Vorwarnung | Hohes Risiko |
| Google-Tagesbudget | Bis 2x Überschreitung pro Tag | Bestätigt |
| Art. 50 AI Act | Seit 02.08.2026: täuschungsgeeignete KI-Produktbilder kennzeichnungspflichtig | Laut Kanzlei-Zusammenfassung |
| Consumer-Abos für Worker | Claude Pro/Max nicht für Agent SDK; ChatGPT Pro mit 5-h- und Wochenlimits | API-Key einplanen |
| Meta Ads MCP | Offiziell seit 29.04.2026, erstellt pausiert, Agent kann aber aktivieren | Aktivierung beim Menschen halten |
| Google Ads MCP | Offiziell, nur lesend | Bestätigt |

## Architekturempfehlung

1. Jetzt: manueller Pilot (Tabelle bzw. dieses Repository plus Patrick).
2. Nach 2 Testzyklen: GitHub Issues + Actions + Environments mit Pflicht-Reviewer als minimaler Controller.
3. Worker bekommt keinen Store-Token mit Publish-Rechten; Seiten als Git-Artefakt.

## Streitpunkte für den Abgleich mit einer unabhängigen Recherche

Claude-Abo und Agent SDK, Meta Ads CLI (pausiert oder aktiv), Codex-Limits, Google Search für Konzeptseiten, Art. 50 AI Act (Leitlinientext nicht selbst geprüft), TikTok Ads MCP, Google Developer Token, Waitlist-Raten, Normnummer Art. 246a EGBGB.
