# Backlog

Owner: **P** = Patrick, **W** = Worker (Claude), **X** = extern.

## Getroffene Entscheidungen

| Datum | Entscheidung | Konsequenz |
|---|---|---|
| 2026-09-26 | **Keine Interviews.** Direkter Weg zum Paid-Concept-Test | Gate 1 auf Basis von Desk-Evidenz und Review-Mining. Das "Warum" kommt aus Qualifizierungsfragen nach dem Opt-in. PR #1 (Interviewleitfaden) geschlossen |

## Offene Entscheidungen für Patrick

Details: `research/2026-09-26-abgleich-claude-chatgpt.md`

| # | Entscheidung | Optionen | Betrifft |
|---|---|---|---|
| D1 | Welche Hypothesen gehen in EXP-001? | (a) 2 Arme nach Review-Mining auswählen; (b) 3 Arme H1, H2, H6 und der Markt entscheidet (etwa 1,5-faches Media-Budget). Vorschlag: (b), weil ohne Interviews der Test selbst die Priorisierung liefern muss | Gate 1 |
| D2 | Primärsignal EXP-001 | Reservierung (braucht Anwalt vorher) oder qualifizierter Opt-in, Reservierung erst in EXP-002. Vorschlag: qualifizierter Opt-in, um nicht auf den Anwalt zu warten | `playbook/fixed.md` |
| D3 | TikTok-Mindestbudget (Kampagne über 50 USD, Ad-Group über 20 USD pro Tag) in feste Regeln aufnehmen | ja / nein | `playbook/fixed.md` |
| D4 | Erster Kanal | Meta, Pinterest oder TikTok, erst nach Kanal-Preflight im Konto | Gate 5 |
| D5 | Media-Budget EXP-001 (Lifetime, gesamt) | Betrag festlegen | Gate 5 |

## Kritischer Pfad zum ersten Paid-Test (Priorität für den Loop)

Nur diese Aufgaben bringen den ersten Test näher. Reihenfolge = Priorität.

| # | Aufgabe | Owner | Liefert |
|---|---|---|---|
| K1 | Review-Mining: 1- bis 3-Sterne-Reviews und Forenbeiträge zu Käse-, Gemüse- und Deckel-Problemen (Amazon.de, Reddit, Foren), mit wörtlichen Zitaten und Datum. Ersatz für die Interviews. **Blockiert:** Netzwerkfreigabe der Umgebung erlaubt Amazon, Reddit, Foren nicht; braucht Patrick: Domains freigeben oder breitere Zugriffsstufe | W | Gate-1-Evidenz, Sprache für Ads und Seiten |
| K2 | Anwalts-Briefing: eine Seite mit konkreten Fragen zu Konzeptseite, KI-Kennzeichnung, Opt-in, Impressum, später Reservierung | W, dann X | Patrick muss nur weiterleiten |
| K3 | Landingpage-Texte H1, H2, H6 in einem einheitlichen Template, mit freigegebenen Formulierungen, Preis, Konzepthinweis und 3 Qualifizierungsfragen nach dem Opt-in (heutige Lösung, letzter Vorfall, bisher ausgegebenes Geld). **Entwurf:** `pages/landingpage-texte-h1-h2-h6.md`; offen: Freigabe [N]-Texte (P), H6-Stückliste (P), Problemzeilen nach K1 belegen | P (Freigabe) | Seite ist in 1 bis 2 Stunden baubar |
| K4 | Ad-Texte und Bild-Briefing je Hypothese (2 Varianten je Arm), passend zur Seite | W | Creatives |
| K5 | Setup-Checkliste Shopify-Konzeptstore: Consent, Double Opt-in, Pixel nach Einwilligung, Impressum, Datenschutz, Conversion-Event | W | Patrick arbeitet sie ab |
| K6 | Vorab-Festlegung EXP-001 als Entwurf (Arme, Metriken, Abbruchregeln), Schwellen als Lücken für Patrick | W | Patrick füllt nur Zahlen aus |
| K7 | Kanal-Preflight-Paket: pro Kanal Ad plus Landingpage zur Richtlinienprüfung im Konto | W, dann P | Kanalentscheidung D4 |
| K8 | Shopify-Konzeptstore aufsetzen | P | Test |
| K9 | Anwalt prüfen lassen | X | Live-Schaltung |
| K10 | Ad-Konto, Budget, Aktivierung | P | Test läuft |

## Zurückgestellt (erst nach EXP-001)

| # | Aufgabe | Owner |
|---|---|---|
| 1 | Tarif klären, API-Key mit Ausgabenlimit | P |
| 3 | Wettbewerbsmatrix auf 30 bis 50 Einträge | W |
| 4b | Käse: technischer Mechanismus (Feuchte-Geruch-Kompromiss). Nur relevant, wenn H2 im Test gewinnt | W, X |
| – | Interviews (verworfen, siehe Entscheidungen) | – |

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
