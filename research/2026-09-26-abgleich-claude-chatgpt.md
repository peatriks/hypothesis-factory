# Abgleich: Claude-Evidenzprüfung vs. ChatGPT Deep Research (26.09.2026)

Quellen:
- **C** = `research/2026-09-26-claude-evidenzpruefung.md`
- **G** = `research/2026-09-26-chatgpt-deep-research.md`

Regel (aus G übernommen): Ein Konflikt wird nicht per Mehrheit aufgelöst, sondern durch die passendere Primärquelle oder einen konkreten Account- bzw. Produkttest.

## Entscheidungsrelevante Widersprüche (Patrick entscheidet)

| # | Aussage | C | G | Ursache der Abweichung | Auflösung durch | Status |
|---|---|---|---|---|---|---|
| 1 | Priorität für Gate 1 | H1 Obst/Gemüse (Rang 1), H2 Käse (Rang 2) | P01 Käse (A), P02 Deckelsystem und Ersatzteile (B), Gemüse nur Alternative (C) | C gewichtet Problembeleg (35 % Abfall) stark; G gewichtet Lernschärfe und Konkurrenzdichte stärker | Interviews je Job, danach Scoring neu kalibrieren | **Offen, Gate 1** |
| 2 | Deckelsystem und Ersatzteile als eigener Job | nur als Nebenjob ("Deckel wiederfinden", Job 11) | eigener Kandidat P02 mit Nutzerbelegen (Reddit BuyItForLife, IKEA-Rezensionen, Pyrex-Ersatzteile) | C hat den Job nicht als Proposition geprüft | Als H6 aufgenommen, Interviews | **Neu: H6** |
| 3 | Erster Paid-Kanal | Meta Link-Ad (mittleres Risiko, Interpretation) | Meta "offen", Richtlinien nicht belastbar ausgewertet; Pinterest oder TikTok Website Lead Gen als prüfbare Pfade | Beide nur Interpretation; G bewertet Meta vorsichtiger | Kanal-Preflight: je Kanal Ad plus Landingpage zur Prüfung im Konto einreichen | **Offen, vor Gate 5** |
| 4 | Primärsignal im ersten Test | Reservierung (voll rückerstattbare Anzahlung) | Bestätigter Opt-in plus qualifizierende Antwort; echte Reservierung erst als späterer, separat freizugebender Schritt | C will früh ein geldnahes Signal; G sieht bei einer Anzahlung höheres Rechts- und Fulfillmentrisiko | Anwaltsprüfung Reservierungsmodell. Wenn nicht rechtzeitig: EXP-001 mit qualifiziertem Opt-in, Reservierung in EXP-002 | **Offen, betrifft playbook/fixed.md** |
| 5 | Käse-Versprechen | VP "jede Sorte im eigenen Klima, kein Austrocknen, kein Geruch" | Verbraucherzentrale rät von luftdichter Käselagerung ab; Kilner löst den Feuchte-Geruch-Kompromiss schon; keine Leistungswörter ohne Mechanismus | C hat die Verbraucherzentrale nicht geprüft | H2-Formulierung entschärfen, technischen Mechanismus vor dem Seitentest klären | **H2 angepasst** |
| 6 | TikTok-Budget | nicht erwähnt | Kampagnenminimum über 50 USD (täglich oder gesamt), Ad-Group über 20 USD pro Tag | Lücke in C | In `playbook/fixed.md` als Bedingung ergänzen (Patrick) | **Befund G übernehmen** |

## Ergänzungen ohne Widerspruch

| Thema | Neu aus G | Wirkung |
|---|---|---|
| Wettbewerb | IKEA 365+ Glas 1 l für 3,79 €, Glas/Bambus 6,29 €; Zwilling Fresh & Save Glas 7-tlg. 84,95 €; Mepal Modula Käse 11,99 €; Mepal Aufschnitt 5,69 €; Kilner Cheese Store £21; Joseph Joseph Nest, Rotho, LocknLock, Pyrex-Ersatzteile | Sehr niedriger Systemanker (IKEA) verschärft die Preisfrage. Premium-Set-Preis um 85 € existiert (Zwilling). Matrix in Backlog #3 zusammenführen |
| Shopify | `pageCreate` akzeptiert `isPublished: true` mit `write_content` oder `write_online_store_pages` | Bestätigt C: Worker bekommt keinen Store-Token mit Seiten-Schreibrecht. Backlog #9 teilweise beantwortet |
| Pinterest API | Status und Zeitplan müssen explizit gesetzt werden, sonst kann eine Kampagne sofort aktiv werden | Prüfpunkt für einen späteren Ads-Adapter |
| Pinterest-Budget | Kann an einzelnen Tagen über dem Tagesbudget liegen | Bestätigt: Stop-Loss nicht über Tagesbudget |
| Shopify Meta Autopilot | Monatsziel ist keine harte Grenze | Nicht als Budgetsteuerung nutzen |
| Recht | Impressum (§ 5 DDG); Datenschutzfragen (Verantwortlicher, Speicherdauer, Auftragsverarbeiter) | Prüfliste ergänzen |
| Gate-Betrieb | Freigabe an Version und Hash binden; kein Approval durch Zeitablauf; doppelter Klick muss idempotent sein | Anforderung für den späteren Controller |
| Messung | Validierungsleiter: Desk Research, Interviews, Concept-Test, Funktionsprototyp, echte Bestellung | Passt zum Pilot |

## Übereinstimmungen (höhere Belastbarkeit)

- Autonome Factory noch nicht bauen; zuerst ein manuell geführter Durchlauf.
- Shopping-, Katalog- und Feed-Formate nicht für ein nicht kaufbares Produkt.
- Google Search für Konzeptseiten riskant bis ungeeignet.
- Tagesbudgets sind keine harte Grenze (Google bis 2x, Pinterest ebenfalls).
- Warteliste ist kein Kaufnachweis.
- 100 Sessions: Wilson-Intervall bei 5/100 etwa 2,2 bis 11,1 bzw. 11,2 %. Nur grobe Richtung.
- Consumer-Abos sind keine verlässliche 24/7-Kapazität; tatsächlichen Tarif prüfen.
- Keine Frische- oder Haltbarkeitsclaims ohne eigenen Test.
- Worker ohne Publish-Credentials; Publizieren nur über ein geschütztes Gate.

## Weiterhin in beiden Berichten offen

Zahlungsbereitschaft über dem Wettbewerb, DE-CPCs, Suchvolumina, Werkzeugkosten und MOQ, eine vollständige SKU-Matrix (30 bis 50), die tatsächliche Freigabe von Concept-Ads im Konto, Art. 50 AI Act im Leitlinientext.

## Hinweis zur Unabhängigkeit

G enthält einen Prüfauftrag für einen unabhängigen Claude-Gegencheck (Abschnitt 15). C ist **nicht** als Antwort auf diesen Auftrag entstanden, sondern auf das ursprüngliche Briefing. Beide Berichte sind also unabhängig voneinander entstanden, aber keiner prüft den anderen gezielt. Ein gezielter Gegencheck nach G Abschnitt 15 ist als Backlog-Eintrag angelegt.
