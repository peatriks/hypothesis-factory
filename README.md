# Hypothesis Factory

Selbstlernendes Test-System für eine Premium-Aufbewahrungsmarke.
Ziel: mit wenig Budget herausfinden, welche Value Proposition echte Kaufabsicht erzeugt.

## Prinzip

Nicht die Ausführung optimiert sich selbst, sondern das **Regelwerk**. Nach jedem Testzyklus
vergleicht das System Vorhersage und Ergebnis und schlägt Änderungen am Playbook vor.
Patrick gibt frei (Pull Request) oder lehnt ab. Das ist der einzige Weg, wie sich das System ändert.

## Drei Schichten

| Schicht | Datei | Wer ändert |
|---|---|---|
| Fest | `playbook/fixed.md` | nur Patrick |
| Lernend | `playbook/learning.md` | System schlägt vor, Patrick gibt frei |
| Ausführend | `hypotheses/`, `experiments/`, `research/` | Worker (anfangs Patrick) |

## Ablauf eines Zyklus

1. **Hypothese** als Karte in `hypotheses/` (Vorlage: `hypotheses/_template.md`)
2. **Vorab-Festlegung** in `experiments/` (Vorlage: `experiments/_template.md`): Vorhersage, Schwellen, Abbruchregeln. Wird vor Teststart committet und danach nicht mehr geändert.
3. **Test** läuft (anfangs manuell)
4. **Ergebnis** wird in dieselbe Experiment-Datei eingetragen
5. **Retro** in `retros/`: Vorhersage gegen Ergebnis, Gate-Entscheidungen, Vorschläge für `playbook/learning.md`
6. **Learnings** mit Evidenz in `learnings.md`

## Autonomer Loop

Eine geplante Routine startet werktags einen Durchlauf nach `ops/LOOP.md`:
Feedback aus Patricks PR-Reaktionen einsammeln, eine Backlog-Aufgabe als PR erledigen,
montags eine Meta-Retro, die Änderungen am eigenen Protokoll vorschlägt (Label `self-change`).
Patrick steuert ausschließlich über Merge, Schließen und Kommentare.

## Status

Phase: **Manueller Pilot** (Start 26.09.2026). Nächste Schritte siehe `BACKLOG.md`.
Quellenstand: `research/`. Zuerst lesen: `research/2026-09-26-abgleich-claude-chatgpt.md` (Abgleich beider Recherchen, offene Entscheidungen).
