# Landingpage-Texte EXP-001: H1, H2, H6

**Stand:** 28.09.2026, Entwurf Worker (Backlog K3). Nicht live. Freigabe durch Patrick und Kanzlei (K2/K9) nötig.
**Annahmen:** D2 = qualifizierter Opt-in (keine Reservierung). D1 = 3 Arme. Ändert Patrick das, fallen Block 6b bzw. ein Arm weg.

**Kennzeichnung jedes Textbausteins:**
- **[F]** freigegebene Formulierung aus `playbook/learning.md#freigegebene-formulierungen`
- **[R]** Formulierung aus der Recherche (`research/2026-09-26-chatgpt-deep-research.md`, 5.1), noch nicht freigegeben
- **[N]** neu vom Worker, **Freigabe durch Patrick nötig** (`playbook/fixed.md`: neue Formulierungen gehen immer über Patrick)

Grenzen aus `playbook/fixed.md`, im Template bereits berücksichtigt: Konzeptstatus, Preis inkl. MwSt. above the fold, Visualisierungs-/KI-Hinweis. Keine Frische- oder Wirkversprechen, keine Streichpreise, kein "auf Lager", "jetzt kaufen", keine Lieferzeit.

---

## 1. Einheitliches Template (für alle Arme gleich)

Reihenfolge ist fix, damit die Arme vergleichbar bleiben. Nur die `{Platzhalter}` ändern sich.

| # | Block | Inhalt | Above the fold |
|---|---|---|---|
| 1 | Badge | **Konzept** | ja |
| 2 | Headline | `{headline}` | ja |
| 3 | Subline | `{subline}` | ja |
| 4 | Bild | `{visual}` mit Bildunterschrift: "Visualisierung (KI-generiert), finales Produkt kann abweichen" [F] | ja |
| 5 | Preiszeile | "Geplanter Preis: `{preis}` € inkl. MwSt. Noch nicht erhältlich." [F, ergänzt um "inkl. MwSt." gemäß `fixed.md`] | ja |
| 6a | Opt-in | Hinweis direkt über dem Formular: "Dieses Produkt ist noch nicht erhältlich. Wir testen derzeit das Interesse am beschriebenen Konzept. Mit deiner Anmeldung erhältst du eine E-Mail, sobald das Produkt startet. Es gibt keine Bestellung und keine Zahlung." [R, Nachrichtentext `[…]` vom Worker gefüllt = N] · Feld E-Mail · Button "Zum Start informieren" [N] · Einwilligungstext: **Platzhalter, kommt von der Kanzlei (K2, Frage 8)** | ja (mobil: direkt unter Preis) |
| 6b | Vorteil | "Frühe Unterstützer erhalten Vorabzugang" [F]. Nur verwenden, wenn "Vorabzugang" konkret definiert ist, sonst streichen | nein |
| 7 | Das Problem | `{problem}` (3 Stichpunkte, beschreiben die Situation, versprechen nichts) | nein |
| 8 | Das Konzept | `{konzept}` (was im Set ist, Material, Status) | nein |
| 9 | Lieferumfang | Tabelle `{set}`: Teile, Maße (soweit definiert, sonst "noch offen"), Material | nein |
| 10 | Was noch offen ist | "Konzept: Wir entwickeln gerade `{kurzname}`." [F] + `{offen}` (Maße, Material, Starttermin) | nein |
| 11 | FAQ | Kann ich das kaufen? "Noch nicht. Es gibt keine Bestellung und keine Zahlung." [R] · Wann startet es? "Einen Termin gibt es noch nicht." [N] · Was passiert mit meiner E-Mail? **Platzhalter Kanzlei** | nein |
| 12 | Footer | Impressum, Datenschutz, Consent-Einstellungen (K5) | nein |

### Nach dem Double Opt-in: Bestätigungsseite mit 3 Qualifizierungsfragen

Freiwillig, nach bestätigter Anmeldung. Überschrift: "Danke. Drei kurze Fragen, damit wir das Richtige bauen (freiwillig)." [N]

| # | Frage [N] | Antworttyp | Zweck |
|---|---|---|---|
| Q1 | "Wie bewahrst du `{gegenstand}` heute auf?" | Auswahl `{q1_optionen}` + "Anders: ___" | Heutige Lösung, Wettbewerbsanker |
| Q2 | "Wann hattest du zuletzt Ärger damit?" | Diese Woche / Diesen Monat / Länger her / Nie | Letzter Vorfall = Schmerzfrequenz |
| Q3 | "Wie viel hast du in den letzten 12 Monaten für `{gegenstand}`-Aufbewahrung ausgegeben?" | 0 € / bis 20 € / 20–50 € / über 50 € / weiß nicht | Bisher ausgegebenes Geld |

Die Preisstufen in Q3 sind Antwortkategorien, keine Marktdaten. Speicherung, Verknüpfung mit der E-Mail und Rechtsgrundlage klärt die Kanzlei (K2, Frage 9).

---

## 2. Arm H1: Obst und Gemüse

Quelle: `hypotheses/H1-produce-frischesystem.md`. Karte erlaubt "sichtbar und trocken", "länger frisch" erst nach eigenem Test.

| Platzhalter | Text | Status |
|---|---|---|
| `{kurzname}` | ein Glas-Set fürs Gemüsefach | N |
| `{headline}` | Obst und Gemüse im Blick, statt ganz hinten im Gemüsefach. | N |
| `{subline}` | Drei Glasbehälter, gemacht fürs Gemüsefach, statt es zu verstopfen. | N (aus VP der Karte abgeleitet) |
| `{preis}` | Arm A: 69 · Arm B: 89 (zufällige Zuteilung, siehe K2 Frage 4) | Karte H1 |
| `{problem}` | • Beeren und Kräuter landen ganz hinten und werden vergessen. • Tüten und Originalschalen sammeln Nässe. • Das Gemüsefach ist voll, aber unübersichtlich. | N, **bis K1 unbelegt** (nicht aus Reviews) |
| `{konzept}` | Drei Glasbehälter in zwei Grundflächen, abgestimmt auf das Gemüsefach. Ein herausnehmbarer Abtropfkorb hält Obst und Gemüse vom Boden fern. Die Belüftung im Deckel lässt sich einstellen. Dazu ein Kräutereinsatz mit Wasserreservoir. | N (aus Produktidee der Karte) |
| `{set}` | 3 Glasbehälter (2 Grundflächen, Maße noch offen) · 3 Deckel mit einstellbarer Belüftung · Abtropfkorb · Kräutereinsatz mit Wasserreservoir | Karte H1 |
| `{offen}` | Genaue Maße, Deckelmaterial und Starttermin stehen noch nicht fest. | N |
| `{gegenstand}` | Obst, Gemüse und Kräuter | – |
| `{q1_optionen}` | Tüte oder Originalverpackung · Frischhaltebox aus Kunststoff · Glasbehälter · Küchenpapier oder Tuch | – |

**Bewusst weggelassen:** "länger frisch", "weniger wegwerfen", "spart Geld" (Wirkversprechen ohne Test, `fixed.md`).

---

## 3. Arm H2: Käse

Quelle: `hypotheses/H2-kaese-sortenbox.md`. VP entschärft; kein "luftdicht", kein "kein Austrocknen" (Verbraucherzentrale, `learnings.md`).

| Platzhalter | Text | Status |
|---|---|---|
| `{kurzname}` | eine Käsebox mit Sortenfächern | N |
| `{headline}` | Mehrere Käsesorten, ein Platz im Kühlschrank. | N |
| `{subline}` | Ein übersichtliches System für mehrere Sorten, das auch auf dem Tisch gut aussieht. | N (aus Arbeitsfassung der Karte, ohne Geruchs-/Feuchteaussage) |
| `{preis}` | 79 | Karte H2 |
| `{problem}` | • Drei offene Käse, drei verschiedene Folien. • Der Geruch vom Bergkäse landet in der Butter. • Zum Servieren wird alles noch einmal umgepackt. | N, **bis K1 unbelegt** |
| `{konzept}` | Eine flache Glasbasis mit zwei bis drei herausnehmbaren Fächern, eines pro Sorte. Ein Deckel, bei dem du die Luftzufuhr einstellen kannst. Aus dem Kühlschrank direkt auf den Tisch. | N (aus Produktidee der Karte) |
| `{set}` | Glasbasis (Maße noch offen) · 3 herausnehmbare Fächer · Deckel mit einstellbarer Luftzufuhr | Karte H2 |
| `{offen}` | Wie die Luftzufuhr technisch funktioniert, testen wir gerade. Maße, Material der Fächer und Starttermin stehen noch nicht fest. | N |
| `{gegenstand}` | Käse | – |
| `{q1_optionen}` | Folie oder Originalverpackung · Käsepapier · Käsedose aus Kunststoff · Käseglocke | – |

**Kritisch für Patrick:** "Der Geruch vom Bergkäse landet in der Butter" beschreibt ein Problem, verspricht aber implizit Geruchsschutz. Alternative ohne Implikation: "Jede Sorte in einer anderen Verpackung." Entscheidung Patrick.
**Bewusst weggelassen:** "luftdicht", "bleibt frisch", "kein Austrocknen", "geruchsdicht".

---

## 4. Arm H6: Wenige Deckel, Ersatz über Jahre

Quelle: `hypotheses/H6-deckelsystem-ersatzteile.md`. **Blocker:** Die Karte verlangt eine exakte Stückliste vor dem Preistest. Unten ein **Vorschlag** mit Lücken, kein festgelegter Umfang.

| Platzhalter | Text | Status |
|---|---|---|
| `{kurzname}` | ein Glasdosen-System mit wenigen Deckelformaten | N |
| `{headline}` | Zwei Deckelgrößen. Jede Dose hat ihren Deckel. | N |
| `{subline}` | Ein Glassystem auf zwei Grundflächen, bei dem du Deckel und Dichtungen einzeln nachkaufen kannst. | N (aus VP der Karte) |
| `{preis}` | Arm A: 89 · Arm B: 119 (Beispielpreise aus der Karte, erst mit Stückliste sinnvoll) | Karte H6 |
| `{problem}` | • Die Deckelschublade ist voll, der passende Deckel fehlt trotzdem. • Nach einem Serienwechsel passt nichts mehr zusammen. • Ein Deckel bricht, und das ganze Set wird unbrauchbar. | N, **bis K1 unbelegt** |
| `{konzept}` | Alle Dosen stehen auf zwei Grundflächen und teilen sich zwei Deckelformate. Deckel und Dichtungen gibt es einzeln zum Nachkaufen. | N |
| `{set}` | **Vorschlag, Patrick legt fest:** `[Anzahl]` Glasdosen in `[Höhen]` auf 2 Grundflächen · `[Anzahl]` Deckel in 2 Formaten · Dichtungen `[austauschbar ja/nein]` · spülmaschinenfest `[offen]` | Lücke |
| `{offen}` | Wie lange es Ersatzteile gibt und zu welchem Preis, legen wir vor dem Start fest. | N |
| `{gegenstand}` | Reste und vorgekochtes Essen | – |
| `{q1_optionen}` | Kunststoffdosen gemischt · Glasdosen (z. B. IKEA) · ein einheitliches Set · Teller mit Folie | – |

**Rechtsrisiko für Patrick:** "einzeln nachkaufen" und "über Jahre" sind Zusagen. Solange keine Ersatzteilpolitik existiert, würde ich die Dauer weglassen (steht so bereits oben: keine Jahreszahl). Kanzlei fragen, ob "nachkaufen" auf einer Konzeptseite bereits bindet.

---

## 5. Messpunkte (für K5 und K6)

| Event | Wann | Zählt als |
|---|---|---|
| Qualifizierte Session | >10 s oder Scroll bis Preiszeile (`fixed.md`) | Nenner |
| Formular abgeschickt | Klick "Zum Start informieren" | nicht Conversion |
| Opt-in bestätigt | Klick im DOI-Mail | **Conversion** (bei D2 = Opt-in) |
| Q1–Q3 beantwortet | Bestätigungsseite | Qualifizierung |

## 6. Offen

- Alle [N]-Texte: Freigabe Patrick. Einwilligungs- und Datenschutztexte: Kanzlei (K2).
- `{problem}`-Zeilen sind Arbeitsannahmen ohne Beleg. Nach K1 durch Formulierungen aus echten Reviews ersetzen.
- H6-Stückliste fehlt. Ohne sie ist der H6-Preis kein sinnvoller Test.
- Bildbriefing für `{visual}` folgt in K4.
