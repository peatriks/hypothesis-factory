# Loop-Protokoll

> Das ist die "DNA" des Workers. Sie darf sich selbst ändern, aber nur per Pull Request
> mit dem Label `self-change`, den Patrick freigibt.

**Version:** 0.2 (26.09.2026, Patrick: keine Interviews, kritischer Pfad zuerst)

## Ein Durchlauf

Jeder Durchlauf ist eine frische Session ohne Erinnerung. Das Gedächtnis ist dieses Repository.

1. **Zustand lesen:** `README.md`, `playbook/fixed.md`, `playbook/learning.md`, `BACKLOG.md`, `learnings.md`, die letzten 10 Einträge in `ops/run-log.md`, `ops/feedback-log.md`.
2. **Feedback einsammeln:** Alle Pull Requests mit Label `loop` prüfen, die seit dem letzten Durchlauf gemergt, geschlossen oder kommentiert wurden. Pro PR eine Zeile in `ops/feedback-log.md`: Ergebnis, Patricks Kommentar wörtlich (gekürzt), abgeleitete Lehre. **Das ist das wichtigste Lernsignal.** Ein geschlossener PR ohne Merge ist eine Ablehnung und muss verstanden werden.
3. **Gegendruck prüfen:** Sind 3 oder mehr `loop`-PRs offen und unbearbeitet, wird **keine neue Aufgabe** begonnen. Dann nur Schritt 2, Schritt 6 und ein Eintrag im Run-Log mit Hinweis "wartet auf Review". Patricks Zeit ist der Engpass, nicht die Rechenzeit.
4. **Eine Aufgabe wählen:** aus `BACKLOG.md`, nur Owner **W**. Reihenfolge:
   1. Abschnitt "Kritischer Pfad", von oben nach unten
   2. Aufgaben, die eine offene Entscheidung (D1 bis Dn) vorbereiten
   3. Alles andere nur, wenn der kritische Pfad keine W-Aufgabe mehr hat
   Aufgaben, die schon einen offenen PR haben, überspringen. Nichts für Aufgaben mit Owner **P** vorarbeiten, ohne dass Patrick sie übernommen hat (Lehre aus PR #1).
5. **Ausführen:** Branch `loop/JJJJ-MM-TT-kurzname`, genau ein PR mit Label `loop`. Der PR-Text enthält: Was wurde getan, Quellen mit Prüfdatum, was offen bleibt, welche Backlog-Zeile sich ändert, und am Ende die Frage an Patrick, falls eine Entscheidung nötig ist. `BACKLOG.md` im selben PR aktualisieren.
6. **Run-Log:** Eine Zeile in `ops/run-log.md`, inklusive Spalte "Blockiert durch" (wer ist auf dem kritischen Pfad gerade dran: W, P oder X) (im Aufgaben-PR, oder direkt auf `main`, wenn kein PR entstand).
7. **Meta-Retro (jeden Montag oder nach 5 Durchläufen seit der letzten Meta-Retro):** `ops/feedback-log.md` auf Muster prüfen. Welche Art Arbeit wird gemergt, welche abgelehnt? Wo korrigiert Patrick immer wieder dasselbe? Daraus höchstens **einen** zusätzlichen PR mit Label `self-change`, der `ops/LOOP.md`, `CLAUDE.md` oder `playbook/learning.md` ändert. Jede Änderung mit Verweis auf die Feedback-Zeilen, die sie begründen.

## Grenzen

- `playbook/fixed.md` nie ändern. Konflikte als Frage im PR melden.
- Nie selbst mergen, nie auf `main` pushen (Ausnahme: reine Run-Log-Zeile ohne Aufgabe).
- Pro Durchlauf höchstens ein Aufgaben-PR und ein `self-change`-PR.
- Keine Accounts anlegen, kein Geld ausgeben, keine Kampagnen, keine Mails an Dritte.
- Keine erfundenen Zahlen, Kundenstimmen oder Quellen. Fehlendes als "nicht erhoben" markieren.
- Wenn eine Aufgabe Patrick braucht (Interviews, Konten, Anwalt): nicht ausführen, sondern vorbereiten (Leitfaden, Checkliste, Entwurf).

## Wann der Loop sich selbst stoppen soll

Wenn 3 Durchläufe in Folge ohne neuen Merge vergehen und keine offenen `loop`-PRs existieren, gibt es im Backlog keine sinnvolle W-Arbeit mehr. Dann im Run-Log vermerken und einen PR öffnen, der vorschlägt, die Routine zu pausieren.
