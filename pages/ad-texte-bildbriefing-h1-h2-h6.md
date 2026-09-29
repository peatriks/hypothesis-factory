# Ad-Texte und Bild-Briefing EXP-001: H1, H2, H6

**Stand:** 29.09.2026, Entwurf Worker (Backlog K4). Nicht live, nichts im Werbekonto angelegt.
**Baut auf:** `pages/landingpage-texte-h1-h2-h6.md` (PR #3, noch nicht gemergt). Ändert Patrick dort Headline, Preis oder Set, ändert sich die Anzeige mit.
**Kanal:** offen (D4). Texte sind kanalneutral; kanalspezifische Pflichten stehen in Abschnitt 4.

Kennzeichnung wie in K3: **[F]** freigegeben (`playbook/learning.md`), **[N]** neu, **Freigabe durch Patrick nötig**.

## 1. Regeln für alle Anzeigen

Aus `playbook/fixed.md` und `research/2026-09-26-claude-evidenzpruefung.md` (Abschnitt 8):

- Anzeige und Landingpage sind inhaltlich deckungsgleich: gleiches Set, gleicher Preis, gleicher Konzeptstatus.
- Jede Anzeige nennt sichtbar **"Konzept"** und **"Noch nicht erhältlich"**, im Text und möglichst im Bild.
- Preis in der Anzeige = Preis der zugeteilten Landingpage-Variante. Bei Preis-Split (H1, H6) je Preisarm eine eigene Anzeige, damit Klick und Seite zusammenpassen.
- KI-Bild: Hinweis "Visualisierung (KI-generiert)" [F] im Bild und im Anzeigentext; TikTok zusätzlich AIGC-Label.
- Verboten: "jetzt kaufen", "auf Lager", Lieferzeit, Streichpreise, Rabatt, Frische- oder Wirkversprechen.
- Call to Action: "Mehr erfahren" (Standard-Button der Plattformen). Kein "Kaufen"/"Shop now".

## 2. Zwei Varianten je Arm

Die Varianten testen die Winkel aus `playbook/learning.md` (Creative-Winkel). Pro Arm: Variante A = Schmerz, Variante B = Genuss bzw. Ordnung. Das ergibt je Arm einen kleinen Winkel-Test innerhalb desselben Seitentemplates.

### H1 Obst und Gemüse

| | A: Schmerz (Verderb) | B: Ordnung/Ästhetik |
|---|---|---|
| Primärtext [N] | Beeren ganz hinten, Kräuter in der Tüte, das Gemüsefach voll und trotzdem unübersichtlich? Wir entwickeln ein Glas-Set, das ins Gemüsefach passt. Konzept, noch nicht erhältlich. Geplanter Preis: `{69/89}` € inkl. MwSt. | Ein Gemüsefach, in dem man alles sieht. Drei Glasbehälter, ein Abtropfkorb, ein Kräutereinsatz. Konzept, noch nicht erhältlich. Geplanter Preis: `{69/89}` € inkl. MwSt. |
| Headline [N] | Obst und Gemüse im Blick | Das Gemüsefach, aufgeräumt |
| Beschreibung | Konzept · Noch nicht erhältlich [F] | Konzept · Noch nicht erhältlich [F] |

### H2 Käse

| | A: Schmerz (Sortenchaos) | B: Genuss/Servieren |
|---|---|---|
| Primärtext [N] | Drei offene Käse, drei verschiedene Folien? Wir entwickeln eine Glasbox mit Fächern für mehrere Sorten. Konzept, noch nicht erhältlich. Geplanter Preis: 79 € inkl. MwSt. | Aus dem Kühlschrank direkt auf den Tisch: eine Glasbasis mit Fächern für mehrere Käsesorten. Konzept, noch nicht erhältlich. Geplanter Preis: 79 € inkl. MwSt. |
| Headline [N] | Mehrere Käse, ein Platz | Käse, servierfertig im Kühlschrank |
| Beschreibung | Konzept · Noch nicht erhältlich [F] | Konzept · Noch nicht erhältlich [F] |

Bewusst ohne Geruchs- oder Frischeaussage (siehe offene Frage 2 in PR #3). "servierfertig" beschreibt die Form, nicht den Käse; Freigabe Patrick.

### H6 Deckelsystem (nur wenn Stückliste steht, siehe PR #3 Frage 1)

| | A: Schmerz (Deckelchaos) | B: Ordnung/Langlebigkeit |
|---|---|---|
| Primärtext [N] | Volle Deckelschublade, und der passende Deckel fehlt trotzdem? Wir entwickeln ein Glasdosen-System mit nur zwei Deckelformaten. Konzept, noch nicht erhältlich. Geplanter Preis: `{89/119}` € inkl. MwSt. | Zwei Deckelgrößen für alle Dosen. Deckel und Dichtungen einzeln nachkaufbar. Konzept, noch nicht erhältlich. Geplanter Preis: `{89/119}` € inkl. MwSt. |
| Headline [N] | Jede Dose hat ihren Deckel | Zwei Deckel, ein System |
| Beschreibung | Konzept · Noch nicht erhältlich [F] | Konzept · Noch nicht erhältlich [F] |

"einzeln nachkaufbar" ist eine Zusage (siehe K2, Anwalts-Briefing). Ohne feste Ersatzteilpolitik Variante B nicht schalten.

## 3. Bild-Briefing

Ein Motiv je Variante. Gleiche Bildsprache über alle Arme, damit der Winkel und nicht die Bildqualität getestet wird.

**Für alle Motive gleich:**
- Format: 1:1 und 9:16 (4:5 optional für Meta-Feed). Pinterest bevorzugt Hochformat; genaue Pixelmaße im Konto prüfen (nicht erhoben).
- Look: echte Küche, Tageslicht, geöffneter Kühlschrank oder Tisch. Keine Studio-Hochglanzoptik, die ein fertiges Produkt vortäuscht.
- Pflicht-Overlay unten links: "Konzept · Visualisierung (KI-generiert)". Gut lesbar, nicht kleiner als der übrige Bildtext.
- Kein Preisschild im Bild mit Streichpreis, kein Lieferhinweis, keine Marke fremder Hersteller erkennbar.
- Produkt nur so zeigen, wie es im Set auf der Landingpage steht (Anzahl Behälter, Fächer, Deckel). Keine Zusatzteile.
- Weg: Bildgenerierung für EXP-001 okay (Moodboard-Qualität), CAD-Rendering erst ab Gate 2 (`research/2026-09-26-claude-evidenzpruefung.md`, Abschnitt 13). Konsistenz zwischen A und B manuell prüfen.

| Arm | Variante | Motiv | Muss sichtbar sein | Darf nicht |
|---|---|---|---|---|
| H1 | A | Gemüsefach von oben: links Tüten, Schalen, ein welkes Kräuterbund; rechts drei Glasbehälter mit Beeren, Salat, Kräutern im Einsatz | Vorher/nachher-Trennung, 3 Behälter, Kräutereinsatz | "Frischer"-Vergleich suggerieren (z. B. welk links, knackig rechts beim gleichen Produkt) |
| H1 | B | Geöffneter Kühlschrank, Gemüsefach mit drei Glasbehältern, alles sichtbar | Glas, Abtropfkorb angedeutet | Überfüllte Deko, die mehr Teile zeigt als das Set |
| H2 | A | Kühlschrankfach mit mehreren angebrochenen Käsen in Folie; daneben die Glasbasis mit drei Fächern | 3 Fächer, Deckel | Schimmel, Kondenswasser als "Problem, das die Box löst" |
| H2 | B | Holztisch, Glasbasis ohne Deckel mit drei Käsesorten, Brot, zwei Gläser Wein | Servierfunktion, Fächer | Anmutung "Käseglocke" oder "luftdicht" |
| H6 | A | Offene Schublade voller unpassender Deckel; daneben ordentlicher Stapel Glasdosen mit zwei Deckelgrößen | 2 Deckelformate, Stapel | Echte fremde Markenlogos auf den Chaos-Deckeln |
| H6 | B | Stapel Glasdosen auf zwei Grundflächen, ein einzelner Ersatzdeckel und eine Dichtung daneben | Ersatzteil als Einzelstück | Jahreszahl, "lebenslang", Garantiesymbol |

## 4. Kanalspezifisch (erst nach D4 relevant)

| Kanal | Zusätzlich beachten | Quelle |
|---|---|---|
| Meta Link-Ad | Keine "deceptive or misleading practices"; Produkt darf nicht "materially differ from what was advertised" | Claude-Evidenzprüfung, Abschnitt 8 |
| Pinterest Standard-Pin | Ad darf nicht suggerieren, dass das Produkt auf der Seite verfügbar ist; "Noch nicht erhältlich" im Pin-Bild | ebd. |
| TikTok In-Feed | AIGC-Label setzen; Preis und Angebot müssen zur Seite passen; Mindestbudget siehe D3 | ebd. und Abgleich #6 |

Zeichenlimits für Primärtext und Headline je Plattform: nicht erhoben. Vor dem Anlegen im Konto prüfen (K7).

## 5. Anzahl Anzeigen

| Arm | Varianten | Preisarme | Anzeigen |
|---|---|---|---|
| H1 | A, B | 69, 89 | 4 |
| H2 | A, B | 79 | 2 |
| H6 | A, B | 89, 119 | 4 |
| **Summe** | | | **10** (6 ohne H6) |

Mehr Anzeigen verteilen das Budget dünner. Ob 10 Anzeigen bei D5 genug Daten je Anzeige liefern, entscheidet die Vorab-Festlegung (K6).

## 6. Offen

- Alle [N]-Texte: Freigabe Patrick.
- H6 hängt an der Stückliste (PR #3, Frage 1) und an der Ersatzteilzusage (K2).
- Problemformulierungen in den A-Varianten sind unbelegt, bis K1 läuft.
- Bilder selbst sind nicht erstellt. Der Worker erzeugt keine Bilder ohne Freigabe von Tool und Kosten.
