# Hypothesen-Test-Factory für eine Premium-Aufbewahrungsmarke: Evidenzprüfung und Empfehlung (Stand 26.09.2026)

Mein Urteil: Patrick sollte die autonome Factory jetzt noch nicht bauen. Zuerst kommt ein manueller Pilot über 4 bis 6 Wochen: zwei klar verschiedene Value Propositions (Obst/Gemüse-Frische und Käse), Meta als erster Paid-Kanal, sichtbarer Preis und als Kaufsignal eine Reservierungsstufe, nicht eine Warteliste. Google Search für eine Konzeptseite ist nach den Google-Richtlinien das riskanteste Element des Briefings. Das Gate-5-Beispiel "Käse / Google Search / 25 € pro Tag" sollte gestrichen oder ans Ende verschoben werden.

## TL;DR

- **Nachfrage:** Der Schmerz ist bei Obst und Gemüse am besten belegt. Laut GfK-Studie 2020 für das BMEL entfallen 35 % der vermeidbaren Lebensmittelabfälle in Haushalten auf frisches Obst und Gemüse. Genau dieses Feld ist aber mit günstigen Speziallösungen besetzt (Tupperware KlimaOase, OXO GreenSaver, Mepal, Zwilling). Ob jemand für schönere Aufbewahrung 79 bis 169 € zahlt, ist völlig unbelegt. Das ist die kritischste Annahme, und ein Wartelisteneintrag beweist sie nicht: Bei physischen Produkten liegen die wenigen öffentlich berichteten Waitlist-to-Purchase-Werte laut Lenny Rachitsky ("conversion rates are all below 5% once you roll your product out widely") unter 5 %.
- **Kanäle und Recht:** Concept-Tests über gewöhnliche Link-Ads bei Meta, TikTok und Pinterest sind nach den Policy-Texten nicht ausdrücklich verboten. Voraussetzung ist, dass Anzeige und Landingpage deckungsgleich sind und die Seite keine Verfügbarkeit suggeriert. Shopping-, Katalog- und Feed-Formate setzen ein kaufbares Produkt voraus. Bei Google Search droht nach der Misrepresentation-Policy im Extremfall eine Kontosperre ohne Vorwarnung. Außerdem gilt seit dem 2. August 2026 Art. 50 AI Act: Fotorealistische KI-Produktbilder, die über das reale Produkt täuschen können, müssen gekennzeichnet werden.
- **Software und Abos:** Claude-Consumer-Abos (Pro, Max) sind für interaktive Nutzung von Claude Code und Claude.ai gedacht. Für unbeaufsichtigte Worker über das Agent SDK verlangt Anthropic einen API-Key. ChatGPT Pro enthält Codex mit rollierenden 5-Stunden- und Wochenlimits, was keinen verlässlichen 24/7-Betrieb trägt. Die Gate-Sicherheit lässt sich über das offizielle Meta-Ads-MCP (mcp.facebook.com/ads, Start 29.04.2026; erstellt Objekte pausiert) und das offizielle Google-Ads-MCP (nur lesend) gut durchsetzen, wenn Aktivierungs- und Budgetrechte in getrennten Credentials beim Menschen bleiben.

## Key Findings

### 1. Evidenzmatrix: Behauptungen aus dem Briefing

| Behauptung aus dem Briefing | Status | Beleg (Prüfdatum 26.09.2026) | Auswirkung aufs System |
|---|---|---|---|
| Es gibt Menschen, die für spezifische Aufbewahrungsprobleme deutlich mehr zahlen | **Ungeklärt** | Das Problem ist belegt (Lebensmittelabfälle, siehe Abschnitt 2). Zur Zahlungsbereitschaft über 50 € für Aufbewahrung habe ich keine Primärquelle gefunden. | Kernhypothese; der erste Test muss sie direkt adressieren |
| Obst/Gemüse ist ein relevanter Schmerzpunkt | **Bestätigt (Problem), ungeklärt (Premium)** | BMLEH/GfK 2020: 35 % der vermeidbaren Haushaltsabfälle sind frisches Obst und Gemüse | Stärkste Problembeleglage, aber günstige Wettbewerber |
| Käse ist ein relevanter Schmerzpunkt | **Teilweise bestätigt** | Viele Speziallösungen im Markt (Zwilling Kühlschrankbox, Mepal Käsedose, Tupperware KäseMax, Käseglocken). Das zeigt Nachfrage, aber auch Sättigung. Bewertungsdaten habe ich nicht systematisch ausgewertet. | Gute Nische, Preisdecke eher niedrig |
| Waitlist-Eintrag beweist keinen Kauf | **Bestätigt** | Lenny Rachitsky ("What is good waitlist conversion", Lenny's Newsletter): "I only have a few data points in this bucket, but conversion rates are all below 5% once you roll your product out widely." | Warteliste nur als Discovery-Signal werten |
| Normale Concept-Ads teilweise möglich | **Teilweise bestätigt (Interpretation)** | Pinterest: Ads dürfen nicht suggerieren, dass ein Produkt auf der Landingpage verfügbar ist, wenn es nicht angeboten wird. TikTok: Ad und Landingpage müssen inhaltlich konsistent sein. Ein explizites Verbot von Konzept- oder Warteliste-Ads habe ich nicht gefunden. | Nur mit klarer Kennzeichnung "Konzept, noch nicht erhältlich" |
| Feedbasierte Shopping-Anzeigen ohne kaufbares Produkt kritisch | **Bestätigt** | Pinterest Merchant Guidelines: Das Produkt muss "available for purchase" sein. Google Merchant Center: Bei Preorder muss die Landingpage das erwartete Lieferdatum zeigen. | Shopping/Feeds erst in der Commerce-Phase |
| Google Search für Konzeptseite (Gate-5-Beispiel) | **Widerlegt als risikoarm** | Google Misrepresentation: nicht erlaubt ist "Offer products or services that you don't have or can't deliver"; Kontosperre "upon detection and without prior warning" | Google Search erst mit Preorder und Lieferdatum |
| Google-Tagesbudget darf bis 2x überschritten werden | **Bestätigt** | Google Ads-Hilfe "Ausgabengrenzen" (answer/10486637): "Bei den meisten Kampagnen ist die Grenze für tägliche Ausgaben Ihr durchschnittliches Tagesbudget multipliziert mit 2"; Monatslimit 30,4x; bei Pay-per-Conversion gibt es "keine Grenze für tägliche Ausgaben" | Stop-Loss nicht über Tagesbudget allein |
| "Claude Premium" als Tarif | **Ungeklärt** | "Premium" gibt es nur als Team-Plan-Seat ("Team (Premium seats)"). Die Consumer-Tarife heißen Pro, Max 5x und Max 20x. | Patrick muss den exakten Tarif in der Abrechnung prüfen |
| Abos tragen 24/7-Worker | **Widerlegt (Claude), eingeschränkt (OpenAI)** | Anthropic: OAuth-Tokens aus Free/Pro/Max in anderen Produkten "including the Agent SDK" nicht erlaubt. OpenAI: 5-Stunden- und Wochenlimits. | API-Budget separat einplanen |
| Gate-Regeln technisch durchsetzbar | **Teilweise bestätigt** | Das offizielle Meta Ads MCP (mcp.facebook.com/ads, 29 Tools, Start 29.04.2026) erstellt Objekte pausiert; laut Passionfruit: "Nothing goes live without a human flipping the activation switch in Ads Manager." Google Ads MCP ist offiziell nur lesend | Aktivierung und Budget beim Menschen lassen |

### 2. Opportunity Landscape: 14 Jobs-to-be-done

Belegquellen: BMLEH/GfK 2020 (35 % Obst und Gemüse, 13 % Brot und Backwaren, 12 % Getränke, 9 % Milchprodukte am vermeidbaren Abfall; 22,4 kg vermeidbare Abfälle pro Person und Jahr, knapp 70 € Einkaufswert; Einpersonenhaushalte 32 kg gegenüber 18 kg in Mehrpersonenhaushalten). Umweltbundesamt: 2023 insgesamt 10,9 Mio. t Lebensmittelabfälle in Deutschland, davon rund 58 % in privaten Haushalten; das UBA beziffert diesen Anteil mit "58 Prozent (6,3 Millionen Tonnen)", was "etwa 74,5 Kilogramm pro Kopf im Jahr" entspricht. Laut der von Statista dargestellten BMEL-Auswertung sind Haltbarkeitsprobleme der häufigste Wegwerfgrund; das überschrittene Mindesthaltbarkeitsdatum folgt erst mit 6 %. Die Einschätzungen "Intensität" und "Premium-Potenzial" sind Schlussfolgerungen, keine Messungen.

| # | Job | Beleglage Problem | Gegenbeleg / Gegenhypothese | Intensität (Einschätzung) | Premium-Potenzial (Einschätzung) |
|---|---|---|---|---|---|
| 1 | Angeschnittenen Käse aufbewahren | Spezialprodukte in allen Preislagen (Zwilling, Mepal, Tupperware, Guzzini, Trendglas Jena); Milchprodukte 9 % des vermeidbaren Abfalls | Käsepapier, Frischhaltefolie und Originalverpackung reichen vielen; Mepal Käsedose im 9-tlg. Set enthalten | Mittel | Mittel (Genießer-Segment) |
| 2 | Obst/Gemüse frisch halten | Stärkste Evidenz: 35 % des vermeidbaren Abfalls | KlimaOase mit Schieberegler und OXO GreenSaver mit Carbon-Filter lösen den Job funktional und günstig | Hoch | Mittel; Differenzierung schwer |
| 3 | Aufschnitt mehrere Tage | Zwilling bewirbt: "Häufig werden Aufschnitt & Co. nur notdürftig verpackt ... Alles wird trocken" (Herstellerclaim) | Günstige Glas-Aufschnittboxen (z. B. KIVY 2er-Set) | Mittel | Niedrig |
| 4 | Rohes Fleisch/Fisch getrennt | Keine spezifische Quelle erhoben | Kurze Lagerdauer, Originalverpackung; hygienische Bedenken gegen Mehrweg | Mittel | Niedrig bis mittel |
| 5 | Meal Prep stapeln/transportieren | Große Glasset-Kategorie (Caraway, Emsa, Zwilling) | Sehr gesättigt, starke Preiskonkurrenz | Mittel | Niedrig |
| 6 | Familie/Kinderportionen | Keine Primärquelle erhoben | Günstige Kunststoffsets dominieren; Kinder und Glas sind ein Konflikt | Mittel | Niedrig |
| 7 | Kleiner Kühlschrank effizient | GfK: Einpersonenhaushalte werfen mehr weg (32 kg gegenüber 18 kg) | Schwacher Zusammenhang zu Behältern | Mittel | Mittel (Raumeffizienz) |
| 8 | Vorräte sichtbar/ordentlich | Mepal Modula (Design Plus Award) etabliert | Gut gelöst; Home-Organization-Suchraum | Niedrig | Mittel |
| 9 | Tägliche Reinigung (Dichtungen) | Mepal-Rezension nennt Wasser im Deckel nach der Reinigung | Zerlegbare Deckel existieren bereits | Mittel | Mittel als Nebenmerkmal |
| 10 | Glas sicher handhaben | Keine systematische Review-Auswertung erfolgt | Borosilikat verbreitet; Bruch selten kaufentscheidend (Annahme) | Unklar | Mittel als Differenzierungsmerkmal |
| 11 | Deckel wiederfinden | Keine Primärquelle erhoben | Nestbare Sets, einheitliche Deckel (Caraway mit Organizern) | Mittel | Mittel (Systemgeschäft) |
| 12 | Ästhetische Küche | DTC-Marken wie Caraway verkaufen explizit "best-looking" Aufbewahrung | Ästhetik ist Designvorliebe, kein Problem; schwache Zahlungsbereitschaftsbasis | Niedrig | Hoch, aber fragil |
| 13 | Haltbarkeit/Reste nachvollziehen | Zwilling Fresh & Save hat einen QR-Code mit App-Tracking | App-Funktionen werden oft nicht genutzt (Annahme, ungeprüft) | Mittel | Niedrig bis mittel |
| 14 | Modular umräumen | Keine Primärquelle erhoben | Kühlschrank-Innenmaße sehr heterogen | Niedrig | Mittel |

**Konsequenz:** Der stärkste Schmerzpunkt (Obst/Gemüse) hat die schwächste Premium-Differenzierung. Die stärkste Premium-Story (Ästhetik, Fridge Architecture) hat den schwächsten Schmerzbeleg. Genau diese Spannung muss der erste Test auflösen.

**Nicht erledigt, aber nötig:** eine systematische Auswertung von Amazon.de-Reviews (1 bis 3 Sterne), Reddit, Foren und YouTube. Suchvolumina habe ich bewusst nicht angegeben, weil keine belastbare Quelle (Google Keyword Planner mit aktivem Konto) vorlag.

### 3. Wettbewerber- und Preismatrix (erfasste Einträge)

Die angestrebte Arbeitsgröße von 30 bis 50 Einträgen habe ich in dieser Recherche **nicht erreicht**. Die Tabelle enthält nur Einträge mit belegtem Lieferumfang. Die Preise stammen von Händlerseiten und Preisvergleichen mit dem genannten Datum und schwanken.

| Marke / Produkt | Exakter Lieferumfang | Preis (Quelle, Datum) | Material | Vertrieb DE | Differenzierung / Kritik |
|---|---|---|---|---|---|
| Zwilling Fresh & Save Vakuum Starterset 17-tlg. | 4 Boxen (S 0,35 l, M 0,9 l, L 2,0 l, Kühlschrankbox 2,0 l), 10 Vakuumbeutel, 3 Bänder | Preis nicht erfasst | Borosilikatglas, Kunststoffdeckel | zwilling.com, Handel | Vakuum mit Indikator; "bis zu 5x länger frisch" (Herstellerclaim, relativ zu Lagerung ohne Vakuum) |
| Zwilling Fresh & Save Vakuumbox S | 1 Box 350 ml | 10,16 bis 11,95 € (tischwelt.de) | Borosilikatglas | Handel | QR-Code-Tracking per App; Pumpe separat |
| Zwilling Fresh & Save Kühlschrankboxset 2-tlg. L | 2 flache Boxen | Preis nicht erfasst | Kunststoff/Glas | zwilling.com | Direkter Wettbewerber für Käse und Aufschnitt |
| Rosti Mepal Modula Starter-Set 5-tlg. | 1x 2000, 1x 1500, 2x 1000, 1x 425 ml (Mengenangabe je nach Quelle abweichend) | Preis nicht erfasst | Kunststoff | culinaris.de, mepal.com | Design Plus Award; für Trockenvorrat |
| Rosti Mepal Modula 7-tlg. | 1x 2000, 2x 1500, 2x 1000, 2x 425 ml | ab 52,94 € (testbericht.de, 04/2026); 63,95 € (eBay-Händler) | Kunststoff | Handel | 3,4/5 aus 50 Bewertungen |
| Rosti Mepal Modula Jubiläums-Set 9-tlg. | 1x 2000, je 2x 1000/1500/425 ml, 1 Käsedose, 1 dreilagige Aufschnittdose | 74,79 € (eBay-Händler) | Kunststoff | Handel | Käse und Aufschnitt im System integriert |
| Rosti Mepal Modula Mini | 1 Dose 175 ml | 16,90 € (eBay-Händler) | Kunststoff | Handel | Anti-Kondens-Einsatz |
| Tupperware KlimaOase 1,8 l hoch | 1 Behälter | 24,90 € (eBay-Händler) | Kunststoff | Beraterinnen, Handel | Schieberegler für Luftzufuhr; genau Job 2 |
| OXO Good Grips GreenSaver Produce Keeper 4,3 Qt | 1 Behälter, Korb, 1 Carbon-Filter | DE-Preis nicht erfasst (US-Handel) | Kunststoff (BPA-frei) | Kaum DE-Präsenz erfasst | Ethylen-Filter, Nachkauf alle 90 Tage (Systemgeschäft) |
| Bosch Vakuum-Frischhaltedose 3-tlg. | 0,9, 1,2 und 1,7 l | ab 46,89 € (testbericht.de) | nicht erfasst | Handel | Vakuum |
| WMF Vorratsdose Depot 1,5 l | 1 Dose | ab 19,95 € (testbericht.de) | nicht erfasst | Handel | Markenpremium über Einzeldose |
| Emsa Clip & Close Glas 4-tlg. | 4 Dosen mit Deckel | Preis nicht erfasst | Glas | OTTO, Handel | "100 % dicht", Massenmarkt |
| Tupperware KäseMax Junior | 1 Käsebehälter | Preis nicht erfasst | Kunststoff | OTTO, Beraterinnen | Laut Vergleichsportal besonders gut verarbeitet (nicht unabhängig geprüft) |
| Caraway Food Storage Set 14-tlg. | 1 groß, 2 mittel, 2 klein, 4 Einsatzdeckel (Dot/Dash), 2 Straps, 3 Organizer | Preis nicht erfasst; kein DE-Vertrieb erfasst | Keramikbeschichtetes Borosilikatglas | US-DTC, US-Retail | Premium-DTC-Referenz; "nicht für Flüssigkeiten auf Reisen" |
| KIVY Glas-Aufschnittbox 2er-Set | 2 flache Boxen, Bambusdeckel | Preis nicht erfasst | Glas, Bambus | Amazon | Marktplatzware, Käse/Aufschnitt |
| Guzzini Gocce / Trendglas Jena Käseglocke | 1 Glocke | Preis nicht erfasst | Kunststoff bzw. Borosilikat + Bambus | Handel | Serviermoment statt Kühlschrankordnung |

**Was die Matrix zeigt:** Premium im DE-Markt liegt heute bei 50 bis 75 € für komplette Kunststoff-Systemsets (Mepal) und bei 10 bis 25 € pro Einzelbehälter (Zwilling, WMF, Tupperware). Ein Käse-Testpreis von 79 € müsste etwa ein Vielfaches einer Einzelbox rechtfertigen. Das ist nur mit einem klar anderen Lieferumfang plausibel (z. B. mehrere Sortenfächer mit Feuchteregelung), nicht mit einer einzelnen schöneren Box. Die Stufen 129 bis 169 € liegen über allem, was ich an DE-Referenzen belegt gefunden habe.

**Offener Rechercheauftrag:** Die Preise von Caraway, Zwilling-Sets und OXO in DE sind nicht erfasst. Weitere Wettbewerber, die auf dieselbe Weise zu prüfen sind: Glasboxen von DTC-Premiummarken, skandinavische Designmarken und Fridge-Organizer von Marktplatz-Brands. Das ist vor Gate 1 von Hand nachzuholen.

### 4. Das "2 Grundflächen × 3 Höhen"-System (Fridge Architecture)

| Frage | Befund | Einordnung |
|---|---|---|
| Neu? | Modulare Stapel- und Rastersysteme existieren: Mepal Modula mit einheitlichem Deckel-/Bodenraster ("sowohl die Unterseite als auch der Deckel bei allen Gr[ößen]" stapelbar laut Rezension), Gastronorm in der Gastronomie | Das Rasterprinzip ist nicht neu. Neu könnte nur die Kombination aus Glas, Silikonschutz, Kühlschrank-Raster und Farbe über Zubehör sein |
| Kühlschrank-Innenmaße | Ich habe keine belastbare Quelle zu Standard-Innenmaßen erhoben | Vor dem Produktkonzept Innenmaße von 10 bis 15 gängigen Einbau- und Standgeräten (Tiefe, Fachhöhe, Türfach) von Hand aus Herstellerdatenblättern sammeln |
| Produzierbar? | Glas und Silikon ist technisch gängig; Werkzeugkosten und MOQ habe ich nicht recherchiert (keine fiktiven Zahlen) | Pro Grundfläche und Höhe entsteht ein eigenes Glaswerkzeug; 2×3 bedeutet mindestens 6 Glaskörper plus 2 Deckelgeometrien. Das kostet ein Vielfaches gegenüber einem Spezialprodukt |
| Patente/Designrechte | Caraway weist auf "one or more patents or patent applications" hin; Zwilling nennt einen "patentierten Vakuum-Deckel" | Freedom-to-operate-Recherche (DPMA/EUIPO/Espacenet) vor Gate 2 durch einen Patentanwalt nötig |
| Wann ist ein Spezialprodukt überlegen? | Wenn der Job eine Funktion braucht, die das System nicht universell liefern kann (Feuchteregelung für Gemüse, Luftaustausch für Käse) | **Empfehlung:** das System als Plattform verstehen, aber mit einem Spezial-Einsatz testen (Produce- oder Käse-Insert in einer Grundfläche) |

### 5. Zahlungsbereitschaft: welche Probleme und welche Tests

| Kandidat für echte Zahlungsbereitschaft | Begründung | Schwäche |
|---|---|---|
| Messbarer Verderb teurer Lebensmittel (Käse, Beeren, Kräuter) | Euro-Wert pro Monat ist greifbar (GfK: knapp 70 € vermeidbare Abfälle pro Person und Jahr) | 70 € pro Jahr über alle Kategorien begrenzt den rationalen Preisrahmen stark |
| Geruch und Hygiene im Kühlschrank | Emotional stark | Schon günstig gelöst |
| Systemkauf für Neueinrichtung (Umzug, neue Küche) | Einmaliger Budgetmoment | Zielgruppe schwer adressierbar |

**Nötige Interviews und Tests (Minimum):** 15 bis 20 problemzentrierte Interviews je Top-Job, geführt nach Mom-Test-Logik: nach dem letzten konkreten Vorfall fragen, nach dem Geld, das schon für Lösungen ausgegeben wurde, und nach aktuellen Workarounds. Keine hypothetischen Fragen. Dazu Review-Mining der 1- bis 3-Sterne-Bewertungen von 10 Wettbewerbern. Erst danach Paid-Tests.

### 6. Material-, Sicherheits- und Herstellungsgrenzen für die Konzepterstellung

| Thema | Befund | Konsequenz für Konzepte |
|---|---|---|
| Rahmenverordnung (EG) 1935/2004 | Keine Abgabe von Bestandteilen in gesundheitsgefährdender Menge; keine geschmackliche oder geruchliche Beeinträchtigung | Konformitätserklärung und Prüfberichte vom Hersteller zwingend |
| Silikon | BfR-Empfehlung XV: höchstens 0,5 % flüchtige organische Bestandteile. Das LGL Bayern fand 2025 bei 3 von 60 Silikon-Backutensilien Werte von 0,7 bis 1,6 %. BfR-Empfehlungen sind laut LGL "keine Rechtsnormen", gelten aber als Stand der Technik | Silikon-Ecken und -Füße nur mit Prüfbericht zu BfR XV (flüchtige Bestandteile, Peroxide); Ausheizen (Tempern) spezifizieren; platinvernetztes Silikon bevorzugen (Herstellerangabe Lindemann) |
| Kunststoffe (Deckel) | VO (EU) 10/2011 gilt für Kunststoff-Lebensmittelkontaktmaterialien (Migration, Konformitätserklärung). Die Details habe ich in dieser Recherche nicht vertieft | Deckelmaterial früh festlegen; Migrationstest einplanen |
| Glas | Borosilikat ist Marktstandard (Zwilling, Caraway, Trendglas) | Thermoschock- und Falltests definieren; Silikonschutz darf keine Hygienefalle (Spalt) erzeugen |
| Reinigung | Zerlegbare Deckel sind bei Mepal ein Rezensionsthema | Keine nicht zerlegbaren Hohlräume; spülmaschinenfest als Mindestanforderung |
| Werbeaussagen | "X-mal länger frisch" ist bei Zwilling ein Herstellerclaim mit Vergleichsbasis | Frische-Claims nur mit eigenem Test; auf Konzeptseiten keine Wirkversprechen |

## Details

### 7. Hypothesis Cards für Gate 1

**Priorisierungsgewichtung (meine Setzung, begründet):** Problemintensität 20 %, Preisplausibilität 20 % (Kernrisiko), Lernwert 15 %, Differenzierung 15 %, Erreichbarkeit 15 %, Produktionskomplexität 10 % (invertiert: einfacher ist besser), Testkosten 5 %. Die Scores (1 bis 5) sind Einschätzungen, keine Messwerte.

| ID | Problem | Preis | Lernwert | Differenz. | Erreichb. | Produktion | Testkosten | Gewichteter Score | Rang |
|---|---|---|---|---|---|---|---|---|---|
| H1 Produce-Frischesystem | 5 | 3 | 5 | 2 | 4 | 3 | 4 | 3,75 | 1 |
| H2 Käse-Sortenbox | 3 | 3 | 4 | 3 | 4 | 4 | 4 | 3,40 | 2 |
| H3 Fridge Architecture Starter-Set | 2 | 2 | 4 | 4 | 3 | 1 | 3 | 2,60 | 4 |
| H4 Geschütztes Glas für Meal Prep | 3 | 3 | 3 | 3 | 4 | 3 | 4 | 3,20 | 3 |
| H5 Aufschnitt-Flachsystem | 3 | 1 | 2 | 2 | 3 | 4 | 4 | 2,40 | 5 |

**H1: Produce-Frischesystem "Crisper Module"**
| Feld | Inhalt |
|---|---|
| Zielgruppe/Kaufkontext | 2- bis 4-Personen-Haushalte mit hohem Frischeanteil (Wochenmarkt, Bio-Kiste), Kauf nach Frust über verdorbene Beeren oder Kräuter |
| Problem und bisherige Lösung | Verderb, Feuchtigkeit, Unsichtbarkeit im Gemüsefach. Bisher: Tüten, Originalschalen, KlimaOase, OXO |
| Beleglage | Für: 35 % des vermeidbaren Abfalls (GfK 2020). Gegen: funktionale Lösungen für 15 bis 25 € existieren |
| Value Proposition | "Obst und Gemüse bleiben sichtbar, trocken und länger frisch, in einem Set, das ins Gemüsefach passt statt es zu verstopfen." |
| Produktidee | 3 Behälter in zwei Grundflächen, herausnehmbarer Abtropfkorb, einstellbare Belüftung, optional Einsatz für Kräuter mit Wasserreservoir |
| Differenzierung | Gegenüber KlimaOase/OXO: Glas statt Kunststoff, Maßraster fürs Gemüsefach, kein Filter-Abo nötig (oder bewusst mit Abo als Systemgeschäft) |
| Testpreis und Umfang | 89 € für 3 Behälter + 1 Kräutereinsatz (Test-Arm A); 69 € als Preis-Arm B |
| Kritischste Annahme | Glas und Design rechtfertigen etwa das 3- bis 4-fache eines Kunststoff-Produce-Keepers |
| Stärkste Gegenhypothese | Frische ist ein Funktionsjob; Käufer wählen das Günstigste, das funktioniert |
| Herstellbarkeit/Compliance | Belüftungsmechanik in Glas/Deckel; Frische-Claims nur mit eigenem Test |
| Kleinster Test | Meta-Link-Ad, 2 Creatives, Landingpage mit Preis-Split 69/89 €, Warteliste plus Reservierungsstufe |
| Lernwert/Unsicherheit | Hoch: prüft direkt, ob der stärkste Schmerz Premium trägt |

**H2: Käse-Sortenbox "Affineur"**
| Feld | Inhalt |
|---|---|
| Zielgruppe/Kaufkontext | Käseliebhaber mit 3 oder mehr Sorten im Kühlschrank, Kauf an der Frischetheke oder als Geschenk |
| Problem und bisherige Lösung | Austrocknen, Geruchsübertragung, Sortenmix. Bisher: Folie, Käsepapier, Mepal-/Tupperware-Käsedose, Zwilling-Kühlschrankbox |
| Beleglage | Für: breites Spezialsortiment zeigt Nachfrage. Gegen: günstige Lösungen, Käsepapier als Low-Tech-Alternative |
| Value Proposition | "Jede Käsesorte bleibt in ihrem eigenen Klima: kein Austrocknen, kein Geruch im Kühlschrank, direkt servierbar." |
| Produktidee | Flache Glasbasis mit 2 bis 3 herausnehmbaren Sortenfächern, Deckel mit Feuchteregelung, Serviertauglichkeit |
| Differenzierung | Gegenüber Mepal/Tupperware: Glas, Sortentrennung, Servierfunktion; gegenüber Käseglocke: kühlschrankfähig und stapelbar |
| Testpreis und Umfang | 79 € für 1 Basis + 3 Fächer + Deckel (Briefing-Preis, bewusst ohne Split beibehalten, um die Hypothese zu prüfen) |
| Kritischste Annahme | Käseliebhaber sind ausreichend groß und über Interessen erreichbar |
| Stärkste Gegenhypothese | Genießer nutzen Käsepapier; Nicht-Genießer zahlen keine 79 € |
| Herstellbarkeit/Compliance | Silikondichtung nach BfR XV; Hygiene der Sortenfächer |
| Kleinster Test | Meta-Interessen-Targeting "Käse/Feinkost", identisches Seitentemplate wie H1 |
| Lernwert/Unsicherheit | Mittel bis hoch; Geschenkkontext separat messen |

**H3: Fridge Architecture Starter-Set**
| Feld | Inhalt |
|---|---|
| Zielgruppe/Kaufkontext | Designaffine Neueinrichter (Umzug, neue Küche) |
| Problem und bisherige Lösung | Unordnung, Platzverschwendung, uneinheitliche Boxen. Bisher: gemischte Sets, Mepal Modula (trocken), Marktplatz-Organizer |
| Beleglage | Für: Ästhetik-DTC existiert (Caraway). Gegen: kein belegter Schmerz, Innenmaße heterogen |
| Value Proposition | "Ein Kühlschrank-Raster aus zwei Grundflächen und drei Höhen, das ohne Tetris passt und über Deckelfarben zur Küche passt." |
| Produktidee | 2 Grundflächen × 3 Höhen, Einheitsdeckel je Grundfläche, Silikonfüße/-ecken, Einsätze optional |
| Differenzierung | Kühlschrankraster statt Vorratsraster (Mepal) |
| Testpreis und Umfang | 149 € für 6 Behälter + 6 Deckel (Mitte der Briefing-Stufen 129/169 €) |
| Kritischste Annahme | Ordnung/Ästhetik erzeugt Zahlungsbereitschaft über 100 € |
| Stärkste Gegenhypothese | Designvorliebe ohne Kaufdruck; hohe Klicks, keine Reservierungen |
| Herstellbarkeit/Compliance | Mindestens 6 Glaswerkzeuge; Patent-/Designrecherche |
| Kleinster Test | Pinterest-Ad (Planungskontext) plus Meta; nur Warteliste und Reservierung |
| Lernwert/Unsicherheit | Hoch für Markenrichtung, niedrig für schnelle Kommerzialisierung |

**H4: Geschütztes Glas für Meal Prep ("Bumper Glass")**
| Feld | Inhalt |
|---|---|
| Zielgruppe/Kaufkontext | Meal-Prepper, Pendler, Familien mit Glaswunsch |
| Problem und bisherige Lösung | Gewicht, Rutschen, Stoß, Bruch. Bisher: Glasbox ohne Schutz, Kunststoff |
| Beleglage | Schwach: keine Review-Auswertung zu Bruch erfolgt (offen) |
| Value Proposition | "Glasboxen, die nicht rutschen, nicht klirren und einen Stoß im Rucksack überstehen." |
| Produktidee | Borosilikat mit abnehmbarem Silikon-Bumper, auslaufsicherer Deckel |
| Differenzierung | Gegenüber Caraway/Emsa/Zwilling: Schutz als Kernmerkmal |
| Testpreis und Umfang | 99 € für 4 Boxen + 4 Deckel + 4 Bumper |
| Kritischste Annahme | Bruch und Handhabung sind häufige Beschwerden in Reviews |
| Stärkste Gegenhypothese | Wer Glas kauft, akzeptiert Gewicht; wer transportiert, nimmt Kunststoff |
| Herstellbarkeit/Compliance | Silikon nach BfR XV; Bumper-Spalt als Hygieneproblem |
| Kleinster Test | Erst Review-Mining (0 € Media); Paid nur bei Belegen |
| Lernwert/Unsicherheit | Mittel |

**H5: Aufschnitt-Flachsystem**
| Feld | Inhalt |
|---|---|
| Zielgruppe/Kaufkontext | Haushalte mit Frischetheke-Einkauf, Verpackungsmüll-sensibel |
| Problem und bisherige Lösung | Austrocknen, Verpackungsmüll, Portionierung. Bisher: Mepal dreilagige Aufschnittdose, Zwilling Kühlschrankbox, KIVY |
| Beleglage | Sehr viele günstige Lösungen |
| Value Proposition | "Aufschnitt von der Theke direkt in flache, stapelbare Glasfächer: frisch, ohne Folie." |
| Produktidee | 3 flache Etagen, gemeinsamer Deckel |
| Differenzierung | Gering |
| Testpreis und Umfang | 59 € für 3 Etagen + Deckel |
| Kritischste Annahme | Premium ist in einer Commodity-Kategorie durchsetzbar |
| Stärkste Gegenhypothese | Preisdecke unter 30 € |
| Herstellbarkeit/Compliance | Einfach |
| Kleinster Test | Nicht als eigenen Paid-Test; als Einsatz in H2 oder H3 prüfen |
| Lernwert/Unsicherheit | Niedrig; **nicht zu Gate 1 vorlegen** |

**Empfehlung Gate 1:** H1 und H2 freigeben, H3 als dritten Arm nur auf Pinterest. H4 erst nach Review-Mining vorlegen, H5 nicht vorlegen.

### 8. Policy-Matrix pro Kanal und Format

Legende: **Concept Test** = klar gekennzeichnetes Konzept, Warteliste, sichtbarer Preis, kein Kauf. **Commerce Test** = kaufbares Produkt oder Preorder mit Lieferdatum. "Interpretation" heißt: Diese Einschätzung ist aus dem Policy-Text abgeleitet und nicht von der Plattform bestätigt.

| Kanal / Format | Concept Test | Commerce Test | Beleg und Unsicherheit |
|---|---|---|---|
| Meta: gewöhnliche Link-Ad (Traffic/Leads-Ziel) | **Möglich, mittleres Risiko** (Interpretation) | Möglich | Meta: Ads dürfen keine Produkte mit "deceptive or misleading practices" bewerben; Community Standard "Prohibited Commercial Practices" nennt "promoting products or services that materially differ from what was advertised". Seitentexte habe ich nur über Suchauszüge geprüft |
| Meta: Lead Ad (Instant Form) | Möglich; Lead Ads Terms müssen akzeptiert werden, Datenschutzlink nötig | Möglich | Die Lead-Ad-Terms-Pflicht ist offiziell belegt, die Details zum Datenschutzlink nur über Dritte. Nachteil: Die Seite mit Preis wird übersprungen, deshalb den Preis in der Ad selbst und im Formular-Intro nennen |
| Meta: Shop Ad / Katalog / Advantage+ Catalog | **Nicht geeignet** | Nach Kaufbarkeit | Katalogformate setzen Produktdaten mit Verfügbarkeit voraus (Analogie zu Google/Pinterest) |
| Pinterest: Standard-/Video-Pin (Traffic, Consideration) | **Möglich nur mit klarer "Noch nicht erhältlich"-Kennzeichnung** | Möglich | Pinterest: "Your ads can't suggest or imply that a product is available on your landing page if you don't actually offer that product." Neue Advertising Guidelines ab 12.11.2026 (Sekundärquelle: Verbot von "dishonest commerce ... deceptive practices") |
| Pinterest: Shopping/Katalog/Product Pins | **Nicht erlaubt** | Nach Kaufbarkeit | Merchant Guidelines: "The Pin must display a specific item ... that is available for purchase"; Preis und Lagerstatus aktuell innerhalb von 7 Tagen |
| TikTok: In-Feed-Ad mit Website-Ziel | **Möglich, mittleres Risiko** (Interpretation) | Möglich | TikTok (Stand April 2026): nicht erlaubt sind "mismatched or inconsistent information on the promotion, price ... including the absence of information". KI-Inhalte brauchen das AIGC-Label, sonst "rejected or restricted" |
| TikTok: Shop/Katalog-Ads | Nicht geeignet | Nach Kaufbarkeit | Nicht vertieft geprüft |
| Google Search (Text-Ads) | **Hohes Risiko** | Möglich mit Preorder, Lieferdatum und Kaufbutton | Misrepresentation: "Offer products or services that you don't have or can't deliver" führt zur Sperre "upon detection and without prior warning". Unavailable Offers: "Promoting products that are not stocked" nicht erlaubt |
| Google Shopping / Merchant Feed / PMax mit Feed | **Nicht geeignet** | Preorder zulässig mit Lieferdatum | Merchant Center: "For 'pre-order' or 'backorder' items, the page must display the expected delivery date"; strukturierte Daten müssen zum Feed passen |
| Amazon/Etsy/Kaufland | Nur Recherche (Reviews, Preise, Suchsprache) | Später | Keine Ads im Konzeptstadium |

**Formulierungen (Interpretation, vor Live juristisch prüfen):**

| Zulässig (niedrigeres Risiko) | Riskant |
|---|---|
| "Konzept: Wir entwickeln gerade ..." | "Jetzt kaufen", "Auf Lager", "Lieferung in 3 Tagen" |
| "Geplanter Preis: 89 €. Noch nicht erhältlich. Trag dich ein, wir melden uns zum Start." | Streichpreise, "-30 %" ohne je verlangten Preis |
| "Visualisierung (KI-generiert), finales Produkt kann abweichen" | Fotorealistische Renderings ohne Hinweis |
| "Frühe Unterstützer erhalten Vorabzugang" | "Hält 5x länger frisch" ohne Test |

**Kann eine ausführliche Konzeptseite bei Google Search beworben werden?** Nach Wortlaut nur mit Risiko. Die Destination Requirements (funktionsfähig, crawlbar, erreichbar; Warnung mindestens 7 Tage vor Sperre) sind erfüllbar. Kritisch ist die Misrepresentation-Policy mit Sperre ohne Vorwarnung, ein Risiko für ein Konto, das Patrick später für die Commerce-Phase braucht. **Empfehlung:** kein Google Search im Concept Test. Falls doch, dann nur mit separatem Google-Ads-Konto und ohne Verknüpfung zum Agenturkonto oder zum späteren Shop-Konto. Und nur, nachdem Google Ads-Support oder -Policy-Team eine schriftliche Einschätzung gegeben hat. Verantwortlich: Patrick als Account-Betreiber.

### 9. Recht DE/EU: Prüfungen vor Ads, Lead-Erfassung und Vorbestellung

| Thema | Anforderung | Stand/Beleg | Wer prüft vor Live |
|---|---|---|---|
| KI-Bild-Kennzeichnung | Art. 50 AI Act gilt seit 02.08.2026 (EU-Kommission, Q&A vom 24.07.2026). Deepfake-Definition Art. 3(60) umfasst Objekte, die "can plausibly exist". Laut Davis+Gilbert-Zusammenfassung der Leitlinien der Kommission gilt ein KI-Produktbild in einer Anzeige, das über Aussehen oder Qualität des realen Produkts täuschen kann, als Deepfake. Der Deployer (Werbetreibende) muss "clear and distinguishable" spätestens beim ersten Kontakt offenlegen. Bußgeld bis 15 Mio. € oder 3 % des Umsatzes | Das Digital Omnibus hat Art. 50(4) laut Sekundärquellen nicht verschoben; nur die Wasserzeichen-Pflicht der Anbieter (Art. 50(2)) hat eine Frist bis 02.12.2026 für Bestandssysteme. Den Wortlaut der Leitlinien habe ich nicht selbst geprüft | Patrick; Rechtsberatung bei Unsicherheit |
| Irreführung (UWG §5, §5a) | Kein Eindruck von Verfügbarkeit; wesentliche Informationen nicht vorenthalten | Dass Konzeptstatus, Preis und Zeitplan klar sichtbar sein müssen, ist Interpretation; der Anhang zu §3 Abs. 3 UWG (Lockangebote) wurde nicht vertieft | Rechtsanwalt (IT-/Wettbewerbsrecht) |
| Preisangaben (PAngV) | Gesamtpreis inkl. MwSt.; die Anwendbarkeit auf ein reines Konzept ohne Angebot ist offen | Nicht vertieft; vorsorglich "inkl. MwSt., zzgl. Versand" angeben | Rechtsanwalt |
| Consent (TDDDG §25, DSGVO) | Pixel und Tags (Meta, TikTok, Pinterest, Google) erst nach Einwilligung; Consent-Banner mit gleichwertiger Ablehnung | Nicht neu recherchiert; etablierte Rechtslage | Patrick (Agenturkompetenz) + Datenschutzprüfung |
| E-Mail-Warteliste | Double Opt-in als Nachweis der Einwilligung; UWG §7 Abs. 2 Nr. 2 verbietet E-Mail-Werbung ohne ausdrückliche Einwilligung | Etablierte Praxis; nicht neu recherchiert | Patrick |
| Vorbestellung/Anzahlung | Art. 246a § 1 Abs. 1 EGBGB verlangt den Termin, bis zu dem geliefert werden muss. LG München I: "bald verfügbar" genügt nicht, die Pflicht gilt auch für nicht vorrätige Artikel. "voraussichtlich" oder "in der Regel" genügen laut Trusted Shops nicht | Die Nummerierung der Norm wird in Quellen unterschiedlich zitiert (Nr. 7 bzw. Nr. 10), bitte am Gesetzestext prüfen. Eine Anzahlung mit Kaufoption kann bereits einen Fernabsatzvertrag auslösen (Widerruf, Informationspflichten) | Rechtsanwalt vor der Reservierungsstufe |
| Lead Ads | Meta Lead Ads Terms; keine sensiblen Daten abfragen | Offiziell belegt | Patrick |

### 10. Experimentdesign: was welches Signal beweist

| Stufe | Misst | Methode | Evidenzstärke |
|---|---|---|---|
| Discovery | Resonanz auf Problem und Creative | CTR, Kosten pro Landingpage-View | Schwach |
| Probleminteresse | Relevanz des Jobs | Scrolltiefe, Klick auf "Wie es funktioniert", Mikro-Umfrage auf der Seite | Schwach bis mittel |
| Preisakzeptanz | Reaktion auf sichtbaren Preis | Preis-A/B (z. B. 69 € vs. 89 €) auf identischer Seite, Randomisierung serverseitig | Mittel |
| Kaufabsicht | Geldnahe Handlung | Zweistufig: nach dem Wartelisteneintrag folgt eine Reservierung (z. B. voll rückerstattbare Anzahlung) | Stark |
| Van Westendorp | Preiskorridor | Nur ergänzend in Interviews/Umfrage; es misst Aussagen, kein Verhalten | Schwach für Kauf |

**Was ein Wartelisteneintrag wert ist (mit Quelle):**
- Lenny Rachitsky ("What is good waitlist conversion", Lenny's Newsletter; Founder-Umfrage): Bei physischen Produkten "I only have a few data points in this bucket, but conversion rates are all below 5% once you roll your product out widely"; bei Paid-Software "5% to 25%, averaging around 20%" bei unter einem Monat Wartezeit und "below 10% if you wait over three months".
- Blazon Agency: freie Signups 1 bis 2 %, 5-$-Deposit 30 bis 50 %. **Vorsicht:** Das ist eine Agentur, die das Deposit-Modell verkauft; Selbstinteresse, keine Methodik offengelegt.
- Waitlister Growth Hub ("7 Waitlist & Product Launch Statistics"): "The typical (median) waitlist converts about 11% of its page visitors into signups"; die Checker-Seite desselben Anbieters nennt dagegen einen Durchschnitt von 13,3 %. Proprietäre Zahlen, laut Anbieter "aren't externally verifiable".
- **Konsequenz:** Eine Warteliste mit 5 % Signup-Rate und darauf unter 5 % Kaufkonversion ergibt Käufe im Promillebereich der Besucher. Die Entscheidungsmetrik muss deshalb die Reservierung sein, nicht der Signup.

### 11. Software und Integration

**Shopify vs. schlanke Landingpage (Konzeptphase)**

| Kriterium | Shopify (Patricks Kernkompetenz) | Framer/Webflow/Carrd/Static + Formular |
|---|---|---|
| Geschwindigkeit für Patrick | Hoch (Expertise, Theme-Vorlagen) | Hoch bei Framer/Carrd |
| Wiederverwendung für Commerce | Hoch: Preorder, Checkout, Feeds später ohne Migration | Niedrig: späterer Umzug |
| Reservierung/Anzahlung | Nativ möglich (Checkout) | Nur über Stripe-Links o. Ä. |
| Agentensicherheit | Admin-API-Scopes granular (read_/write_ je Ressource); "no dry-run mode" laut Drittanbieter-MCP-Guide | Statisches Hosting: Git-PR als natürliches Draft-Gate |
| Kosten | Nicht neu recherchiert; Patrick kennt die Tarife | Nicht recherchiert |

**Empfehlung:** Shopify verwenden, weil die Reservierungsstufe den Checkout braucht und die Commerce-Phase darauf aufbaut. Die Konzeptseiten sollten als eigene Seiten oder Templates im gleichen Store laufen, getrennt von Patricks Agentur-Stores.

**Shopify-MCPs/APIs**

| Baustein | Kann | Kann nicht / Risiko | Beleg |
|---|---|---|---|
| Shopify Dev MCP (@shopify/dev-mcp) | Doku-Suche, Schema-Introspektion, GraphQL-/Liquid-Validierung; braucht keine Store-Credentials | Keine Store-Aktionen | Sekundärquellen (claudefa.st, letstalkshop) |
| Shopify AI Toolkit / CLI `shopify store execute --allow-mutations` | Führt Admin-Mutationen aus | "The change is live immediately"; kein Draft-Modus | Sekundärquelle (fudge.ai) |
| GraphQL Admin API | Alle Admin-Aktionen je nach Scope; Scopes lassen sich per `appRevokeAccessScopes` reduzieren | Throttling (laut Sekundärquelle 50 Kostenpunkte/Sekunde) | shopify.dev |
| Storefront MCP | Käuferseitige Abfragen | Keine Admin-Schreibrechte | Nicht vertieft |

**Draft vs. Publish technisch trennen (Empfehlung, vor Umsetzung in shopify.dev verifizieren):**
- Worker-App bekommt nur `write_content`/`write_themes` auf einem **unveröffentlichten Theme** bzw. Seiten mit `published: false`.
- Das Veröffentlichen (Theme publish, Page publish, Preisänderung) läuft über eine zweite App-Identität, deren Token nur der Controller nach Gate-4-Freigabe nutzt.
- Einschränkung: Ob Shopify-Scopes "Theme bearbeiten" und "Theme veröffentlichen" trennen, habe ich **nicht verifiziert**. Wahrscheinlich nicht, dann ist der Scope `write_themes` für beides nötig. Die Trennung muss dann über den Controller erfolgen: Der Worker bekommt überhaupt keinen Store-Token, sondern liefert Theme-Dateien als Git-Artefakt. Das ist die robustere Lösung.

**Ads-Plattformen: Draft, Publish, Pause, Budget**

| Plattform | Offizieller Agentenzugang | Draft/Pause | Aktivieren/Budget | Zugangsvoraussetzung | Beleg |
|---|---|---|---|---|---|
| Meta | Offizielles Ads MCP (mcp.facebook.com/ads) und Ads CLI, gestartet am 29.04.2026, 29 Tools | Objekte über MCP werden pausiert erstellt | Agent kann nachträglich aktivieren | Business-OAuth, laut Sekundärquellen kein App Review | Laut AdsUploader sagt die aktuelle Meta-Doku zur Ads CLI: "campaigns, ad sets and ads are created paused by default, with creatives the one exception"; ein Agent kann sie danach aktivieren. Eine andere Sekundärquelle (Soku) behauptet, die CLI erstelle standardmäßig aktiv |
| Google Ads | Offizielles Google Ads MCP (Open Source, self-hosted): 3 Tools, **nur lesend** | Nicht über MCP | Nur über Google Ads API oder UI | Developer Token mit Basic Access (Design-Dokument); Google stellt laut Doku auf API-Aufrufe ohne Developer Token um (Übergangsphase) | developers.google.com; GitHub-Issue #50 |
| TikTok | Ads MCP Server und Ads Skills laut Sekundärquelle öffentlich seit 12.05.2026 | Nicht verifiziert | Nicht verifiziert | Nicht verifiziert | palai.media (Sekundär) |
| Pinterest | Nicht recherchiert | | | | Offen |
| Shopify-Kanal-Apps (Meta, Google, Pinterest, TikTok) | Verbinden primär Feed/Pixel/Katalog | Kampagnensteuerung eingeschränkt | Nicht als Budgetsteuerung nutzen | | Nicht vertieft; als "Feed/Pixel verbinden" behandeln |

**Die drei Fähigkeiten getrennt (wie im Briefing gefordert):** (1) Feed/Pixel verbinden: Shopify-Kanal-Apps, einmalig, Mensch. (2) Kampagne erstellen: Meta-MCP pausiert, Worker darf das. (3) Volle agentische Steuerung inklusive Budget und Status bleibt beim Menschen. Meta erlaubt technisch das Aktivieren per Agent. Deshalb muss der Worker-Token so eingeschränkt oder vermittelt sein, dass er nicht aktivieren kann. Ob das offizielle MCP Aktivierung und Erstellung auf Token-Ebene trennt, ist **nicht belegt**. Ein Community-Server (safe-meta-ads-mcp, GitHub oussch702) erzwingt die Trennung: Laut README braucht jede Aktivierung "the exact phrase ACTIVATE AND ALLOW SPEND", und bei gesetztem Tagesbudget-Maximum "it refuses anything that would take a campaign above it". Er ist aber ungeprüfter Drittanbieter-Code.

**Architekturoptionen**

| Option | Persistenz/Zustand | Rechte | Mobile Gates | Eigenbau | Betrieb | Einschätzung |
|---|---|---|---|---|---|---|
| A: Manueller Pilot (Notion/Sheet + Patrick) | Tabelle | Patrick allein | Entfällt | Keiner | Einfach | **Jetzt starten** |
| B: GitHub Issues + Actions + Environments mit Pflicht-Reviewern | Issues/Labels = Zustand; Repo = Artefakte | Secrets pro Environment; Publish-Jobs nur nach Review | GitHub-Mobile-App für Approvals | Gering | Mittel | **Empfohlener minimaler Controller** (Environment-Reviewer-Mechanik vor Umsetzung verifizieren) |
| C: n8n (self-hosted) + Postgres + Telegram-Bot | Workflows + DB | Credentials zentral in n8n (Risiko: ein Ort für alles) | Telegram-Buttons | Mittel | Wartung, Sicherheitsupdates | Gut für Integrationen, schwächer bei Audit |
| D: Temporal + eigener Factory-MCP + Supabase | Durable Workflows | Sauber trennbar | Eigenbau | Hoch | Hoch | Überdimensioniert für die Testphase |
| E: Airtable + Automations | Tabelle | Grob | Airtable-App | Gering | Einfach | Für den Pilot okay, Rechte zu grob |

**Klare Empfehlung zum Pilot:** Ja, der manuelle Pilot vor eigener Orchestrierung senkt das Risiko schneller. Die größten Risiken liegen in Nachfrage, Preis, Policy und Recht, nicht in der Orchestrierung. Der Pilot beantwortet sie in Wochen. Eine Factory automatisiert bis dahin nur einen Prozess, dessen Entscheidungsregeln noch unbekannt sind. Dass Telegram-Gates auf GitHub-Environments aufsetzen, lohnt sich erst, wenn mehr als etwa 3 Propositions pro Monat getestet werden.

### 12. Abos vs. API: Eignung für 24/7-Automation

| Abo | Enthalten | Nicht enthalten / Grenze | Beleg (Stand) | Konsequenz |
|---|---|---|---|---|
| Claude Pro / Max 5x / Max 20x | Interaktives Claude Code, Claude.ai | Laut Anthropic-Doku (seit 19.02.2026): OAuth aus Free/Pro/Max "in any other product, tool, or service, including the Agent SDK, is not permitted" | code.claude.com / Legal and Compliance, über Sekundärzitate | Für unbeaufsichtigte Worker API-Key (Claude Console) nutzen |
| Claude Agent SDK / `claude -p` / GitHub Actions mit Abo | Help Center (Update 15.06.2026): geplante Änderungen pausiert; "Claude Agent SDK, `claude -p`, and third-party app usage still draw from your subscription's usage limits" | Der angekündigte Monats-Credit ist "isn't available". Für Teams: "shared production automation should use Claude Platform with an API key" | support.claude.com, 16.06.2026 | **Widerspruch** zwischen Help Center und Legal-Doku, deshalb konservativ API-Key |
| Claude Team (Standard/Premium seats) | Team-Nutzung | Premium-Seat vermutlich Patricks "Claude Premium" | support.claude.com (Credit-Tabelle nennt "Team (Premium seats)") | Tarif in der Abrechnung prüfen |
| ChatGPT Pro (laut Sekundärquellen ab 100 $, 5x, oder 200 $, 20x) | Codex lokal (CLI/IDE) und Cloud, geteiltes Kontingent | Rollierendes 5-Stunden-Fenster und Wochenlimit; Cloud-Tasks verbrauchen mehr. Am 12.07.2026 wurde das 5-Stunden-Limit temporär aufgehoben und am 30.07.2026 wieder eingeführt (Sekundärquelle) | help.openai.com, developers.openai.com/codex/pricing | Kein verlässlicher 24/7-Durchsatz; API-Key = API-Preise |
| OpenAI-Nutzungsbedingungen zu Automation | Nicht geprüft | | Offen | Vor dem Bau prüfen |

**Kosten- und Risikoübersicht (monatlich, nur belegte oder vom Nutzer bekannte Posten)**

| Posten | Betrag | Status |
|---|---|---|
| Claude Max 5x / 20x | 100 $ / 200 $ (Sekundärquelle) | Vorhanden bzw. zu prüfen |
| ChatGPT Pro | ab 100 $ bzw. 200 $ (Sekundärquelle) | Vorhanden |
| Claude API (Worker) | Nutzungsbasiert, nicht beziffert | **Neu einplanen**, Budget-Limit in der Console setzen |
| OpenAI API | Nutzungsbasiert | Optional |
| Shopify-Plan, Apps, Consent-Tool | Nicht recherchiert | Patrick bekannt |
| Rechtsberatung (einmalig) | Nicht recherchiert | Vor der ersten Live-Schaltung |
| Media-Budget Pilot | Vom Nutzer festzulegen (Vorschlag siehe unten) | Gate 5 |

### 13. Konsistente Produktvisualisierung

| Weg | Konsistenz über Creatives | Aufwand | Wann sinnvoll |
|---|---|---|---|
| Reine Bildgenerierung (GPT-Image u. a.) | Niedrig: Proportionen und Details driften zwischen Bildern | Gering | Moodboards, frühe Gate-2-Skizzen |
| Einfaches CAD (Onshape/Blender) + Rendering, KI nur für Szene/Hintergrund | Hoch: ein Geometriemodell für alle Formate | Mittel | **Ab Gate 2 empfohlen**, weil Maße (Kühlschrankraster) ohnehin festgelegt werden müssen |
| KeyShot/Spline-Hochglanzrenderings | Hoch | Höher | Commerce-Phase |

Bezug zu Art. 50 AI Act: Ein echtes CAD-Rendering mit KI-Hintergrund ist nach der von Davis+Gilbert berichteten Leitlinienlogik weniger kritisch, solange das Produkt nicht irreführend dargestellt wird. Fotorealistische KI-Produktbilder sind kennzeichnungspflichtig. Die Tool-Kosten habe ich nicht recherchiert.

## Recommendations

### 14. Erster aussagekräftiger Test (Vorschlag für Gate 5)

| Parameter | Vorschlag | Begründung |
|---|---|---|
| Propositions | H1 (Produce) und H2 (Käse), identisches Seitentemplate | Vergleich Schmerz- vs. Genuss-Job |
| Kanal | Meta (Facebook/Instagram), Link-Ad mit Ziel Landingpage-Views | Policy-Risiko mittel, Agentenzugang pausiert; Google Search entfällt |
| Seite | Shopify, "Konzept"-Badge, Preis above the fold, KI-/Render-Hinweis, Warteliste (Double Opt-in), danach Reservierungsschritt (erst nach Rechtsprüfung) | Trennt Signup von Kaufabsicht |
| Preis-Arme | H1: 69 € vs. 89 €; H2: 79 € | Preisakzeptanz |
| Budget | Pro Proposition zunächst ein fester Lifetime-Betrag auf Kampagnenebene plus Kontoausgabenlimit bei Meta | Hartes Stop-Loss statt Tagesbudget |
| Datenmenge | Rechenbeispiel: Bei 100 Sessions und 5 Signups liegt das 95-%-Wilson-Intervall bei etwa 2,2 bis 11,1 %. 100 Sessions reichen also nur, um sehr schlechte von sehr guten Seiten zu trennen | Das Briefing-Ziel "100 relevante Sessions" ist für Preis-A/B-Vergleiche zu klein |
| CPC | Keine belastbare DE-Home/Kitchen-Quelle gefunden. Das Briefing impliziert 175 € / 100 Sessions = 1,75 € je Session als Obergrenze | Echte Kosten pro Landingpage-View nach 48 Stunden messen, dann Budget neu entscheiden |

**Vor Testbeginn fixieren:**
- Primärmetrik: Reservierungen je 100 Landingpage-Views. Sekundär: Signups je 100 Views, Kosten pro Signup.
- Qualifikation: nur Sessions mit mehr als 10 s Verweildauer oder Scroll bis zum Preis gelten als "relevant". Bots und interne IPs ausschließen.
- Kontrollvariablen: identisches Template, Creative-Paar, Targeting, Laufzeit, Wochentage, Gerätemix berichten.
- Abbruch: Budget erschöpft; Policy-Ablehnung; Tracking-Ausfall (0 Events über 6 Stunden bei laufendem Spend); CPC deutlich über der vorab definierten Obergrenze nach 48 Stunden.
- Entscheidungsregel (Beispielschwellen, vor Start von Patrick festzulegen): KEEP nur bei Reservierungen über einer festgelegten Mindestzahl. Signups ohne Reservierungen bedeuten ITERATE (Preis oder Angebot), nicht KEEP.

### 15. Spend-Kontrolle technisch

| Ebene | Mechanismus | Beleg |
|---|---|---|
| Google | Durchschnittliches Tagesbudget: bis 2x pro Tag ("Bei den meisten Kampagnen ist die Grenze für tägliche Ausgaben Ihr durchschnittliches Tagesbudget multipliziert mit 2"), 30,4x pro Monat; bei Pay-per-Conversion "keine Grenze für tägliche Ausgaben"; Überlieferung wird nicht berechnet. Bei Ad Scheduling pacet Google auf das volle Monatslimit | Google Ads-Hilfe "Ausgabengrenzen" (answer/10486637) |
| Google Konto | Monatliches Kontolimit / Kontobudget (Sekundärquelle 7ten) | Vor Einsatz in der Google-Hilfe verifizieren |
| Meta | Kampagnen-Lifetime-Budget, Kontoausgabenlimit | Nicht neu recherchiert, Standardfunktion; verifizieren |
| Controller | Unabhängiger Watchdog pollt die Reporting-API und pausiert bei Grenzverletzung; Reporting-Verzögerung einplanen (nicht quantifiziert belegt) | Pausieren sollte als einzige Schreibaktion automatisch erlaubt sein |

### 16. Automatisierbar vs. menschlich

| Automatisierbar (Worker) | Mensch/Extern |
|---|---|
| Review-Mining, Clustering, Wettbewerbstabellen | Gate-1- bis Gate-5-Entscheidungen (Patrick) |
| Landingpage-Entwürfe als Git-Artefakt | Rechtliche Freigabe der Seitentexte (Anwalt, einmalig pro Template) |
| QA: Links, Consent-Blocking vor Einwilligung, Formular-Double-Opt-in, Preis sichtbar vor dem Formular | Konto-Setup, Business-Verifizierung, Zahlungsmittel (Account-Betreiber) |
| Pausierte Kampagnenentwürfe (Meta MCP) | Aktivierung und Budget (Patrick) |
| Reporting und Entscheidungsvorlage | CAD-Modell/Design (Designer), Machbarkeit und Kosten (Hersteller), Patentrecherche (Patentanwalt) |

### Nächste Schritte (Reihenfolge)
1. Tarif klären: "Claude Premium" gleich Team Premium Seat oder Max? Dann API-Key mit Ausgabenlimit anlegen.
2. Zwei Wochen Review-Mining und 15 bis 20 Interviews zu H1/H2.
3. Anwalt: Template-Freigabe für Konzeptseite, KI-Kennzeichnung, Reservierungsmodell.
4. Shopify-Konzeptstore, Consent, Double Opt-in, Meta-Pixel erst nach Einwilligung.
5. Meta-Test H1/H2 manuell anlegen (pausiert, dann Patrick aktiviert).
6. Erst nach 2 abgeschlossenen Testzyklen: GitHub-basierter Controller (Option B).

## Caveats

### Offene Fragen ohne sichere Quellenantwort
- Ob Meta/TikTok Concept-Ads mit Warteliste in DE in der Praxis ablehnen (keine explizite Regel gefunden; Praxisrisiko unbekannt).
- Ob das offizielle Meta Ads MCP Erstellen und Aktivieren auf Berechtigungsebene trennt.
- Ob Shopify-Scopes Theme-Bearbeitung und -Veröffentlichung trennen.
- Belastbare CPC/CPM-Bandbreiten DE für Home/Kitchen (keine Quelle gefunden, bewusst keine Zahlen).
- Werkzeugkosten, MOQ und Stückkosten für Glas/Silikon (keine Quellen, bewusst keine Zahlen).
- DE-Preise von Caraway, Zwilling-Sets und OXO; 30 bis 50 Wettbewerbereinträge noch nicht erreicht.
- OpenAI-Nutzungsbedingungen zu automatisierter Nutzung von ChatGPT-Pro/Codex.
- PAngV- und UWG-Anhang-Anwendbarkeit auf reine Konzeptseiten.

### Voraussichtliche Streitpunkte für den Abgleich mit einer unabhängigen ChatGPT-Recherche
| Streitpunkt | Warum unsicher |
|---|---|
| Claude-Abo mit Agent SDK / `claude -p` / GitHub Actions erlaubt? | Help Center (15.06.2026) sagt, die Nutzung zählt weiter auf Abo-Limits; die Legal-Doku (Februar 2026) verbietet OAuth im Agent SDK |
| Meta Ads CLI: Standard pausiert oder aktiv? | AdsUploader zitiert die Meta-Doku mit "created paused by default, with creatives the one exception"; Soku behauptet dagegen, die CLI erstelle standardmäßig aktiv |
| Codex 5-Stunden-Limit aktuell aktiv? | Temporäre Aufhebung am 12.07. und Wiedereinführung am 30.07.2026 nur über Sekundärquellen belegt |
| Google Search für Konzeptseiten | Die Policy-Wortlaute sprechen dagegen; Praxisberichte könnten Toleranz zeigen |
| Art. 50 AI Act für KI-Produktbilder | Die Kernaussage stammt aus der Zusammenfassung einer Kanzlei, nicht aus dem Leitlinientext selbst; das Digital-Omnibus-Datum (VO 2026/1744) wurde nicht auf EUR-Lex verifiziert |
| TikTok Ads MCP Verfügbarkeit | Nur eine Sekundärquelle |
| Google Developer Token | Die Google-Doku spricht von einer Abschaffung der Developer Tokens in API-Aufrufen; ältere Guides verlangen den Token weiterhin |
| Waitlist-Konversionsraten | Alle Werte stammen aus Umfragen oder Anbieterdaten mit Eigeninteresse; keine peer-reviewte Quelle |
| Norm-Nummer Lieferzeit (Art. 246a § 1 Abs. 1 Nr. 7 vs. Nr. 10 EGBGB) | Quellen zitieren unterschiedlich |
