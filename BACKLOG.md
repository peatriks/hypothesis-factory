# Backlog

Wird zu GitHub Issues, sobald das Repository steht. Owner: **P** = Patrick, **W** = Worker (Claude), **X** = extern.

## Entscheidungen für Patrick (aus dem Abgleich beider Recherchen)

Details: `research/2026-09-26-abgleich-claude-chatgpt.md`

| # | Entscheidung | Optionen | Betrifft |
|---|---|---|---|
| D1 | Welche Hypothesen gehen in die Interviews? | Claude: H1 + H2. ChatGPT: Käse (H2) + Deckelsystem (H6), Gemüse als Alternative. Vorschlag: H1, H2 und H6 in die Interviews, erst danach Gate 1 | Gate 1 |
| D2 | Primärsignal EXP-001 | Reservierung (braucht Anwalt vorher) oder qualifizierter Opt-in, Reservierung erst in EXP-002 | `playbook/fixed.md` |
| D3 | TikTok-Mindestbudget (Kampagne über 50 USD, Ad-Group über 20 USD pro Tag) in feste Regeln aufnehmen | ja / nein | `playbook/fixed.md` |
| D4 | Erster Kanal | Meta, Pinterest oder TikTok, erst nach Kanal-Preflight im Konto | Gate 5 |

## Jetzt (Pilot, vor dem ersten Test)

| # | Aufgabe | Owner | Blockiert |
|---|---|---|---|
| 1 | Tarif klären ("Claude Premium" = Team Premium Seat oder Max?), API-Key mit Ausgabenlimit anlegen | P | Automatisierung |
| 2 | Review-Mining: 1- bis 3-Sterne-Reviews von etwa 10 Wettbewerbern clustern (Amazon.de, Reddit, Foren) | W | H4, Schärfung H1/H2 |
| 3 | Wettbewerbsmatrix auf 30 bis 50 Einträge: beide Recherchen zusammenführen (u. a. IKEA 365+, Joseph Joseph, Rotho, Kilner, LocknLock, Pyrex neu aus ChatGPT), einheitliches Raster (Größe, Material, Footprint, Dichtung, Ersatzteile, UVP/Aktion). DE-Preise Caraway, OXO fehlen noch | W | Preisplausibilität |
| 4 | Interviews je Job (Claude: 15 bis 20, ChatGPT: 10 bis 15 als Arbeitsziel), Mom-Test-Logik, für H6 Deckelinventar abfragen. Vorher Gate-1-Schwellen im Leitfaden (Abschnitt 8) setzen | P | Gate 1 |
| 4a | Interviewleitfaden für H1, H2, H6: Entwurf v0.1 in `interviews/leitfaden-h1-h2-h6.md`, nach den ersten 3 Interviews schärfen | W | #4 |
| 4b | Käse: technischer Mechanismus für den Feuchte-Geruch-Kompromiss, Vergleich mit Kilner, Mepal, Rotho, Käsepapier | W, X (Produktentwickler) | H2 |
| 5 | Anwalt: Template-Freigabe Konzeptseite, KI-Kennzeichnung, Reservierungsmodell | X | Live-Schaltung |
| 6 | Shopify-Konzeptstore, Consent, Double Opt-in, Meta-Pixel nach Einwilligung | P | Test |
| 7 | Schwellen für EXP-001 festlegen | P | Test |

## Offene Rechercheaufgaben (aus Caveats)

| # | Frage | Owner |
|---|---|---|
| 8 | Trennt das offizielle Meta Ads MCP Erstellen und Aktivieren auf Berechtigungsebene? | W |
| 9 | Trennen Shopify-Scopes Theme-Bearbeitung und -Veröffentlichung? Teilantwort: `pageCreate` kann mit `write_content` direkt veröffentlichen, also kein Seiten-Schreibrecht für den Worker | W |
| 10 | CPC/CPM-Bandbreiten DE Home/Kitchen | W, nach erstem Test aus eigenen Daten |
| 11 | Werkzeugkosten, MOQ, Stückkosten Glas/Silikon | X (Hersteller) |
| 12 | OpenAI-Nutzungsbedingungen zu automatisierter Nutzung | W |
| 13 | PAngV/UWG-Anhang auf reine Konzeptseiten | X (Anwalt) |
| 14 | Innenmaße von 10 bis 15 gängigen Kühlschränken | W |
| 15 | Kanal-Preflight: je Kanal ein Ad-plus-Landingpage-Paar im Konto zur Richtlinienprüfung vorbereiten | P, W |
| 16 | Gezielter Gegencheck nach Prüfauftrag in ChatGPT-Recherche, Abschnitt 15 | W |
| 17 | Datenschutz: Verantwortlicher, Rechtsgrundlage, Auftragsverarbeiter, Speicherdauer der Warteliste | P, X |

## Später (nach 2 abgeschlossenen Testzyklen)

- GitHub-basierter Controller (Issues + Actions + Environments mit Pflicht-Reviewer)
- Watchdog, der bei Grenzverletzung pausiert
