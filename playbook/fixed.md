# Playbook: feste Regeln

> Diese Datei ändert nur Patrick. Retros dürfen Änderungen hier **nicht** vorschlagen,
> nur Konflikte melden ("Regel X hat Test Y blockiert").

## Ziel und Primärmetrik

- **Primärmetrik:** Reservierungen je 100 qualifizierte Landingpage-Views.
- Sekundär: Signups je 100 Views, Kosten pro Signup, Kosten pro Landingpage-View.
- Signups ohne Reservierungen bedeuten nie KEEP, höchstens ITERATE.
- Qualifizierte Session: mehr als 10 s Verweildauer oder Scroll bis zum Preis. Bots und interne IPs ausgeschlossen.

## Geld

- Aktivieren von Kampagnen und Ändern von Budgets: **nur Patrick**.
- Automatisch erlaubte Schreibaktion: **Pausieren**.
- Stop-Loss über Lifetime-Budget auf Kampagnenebene plus Kontoausgabenlimit, nie nur über Tagesbudget (Google überschreitet Tagesbudgets bis 2x).
- Claude API mit Ausgabenlimit in der Console. Keine Consumer-Abos für unbeaufsichtigte Worker.

## Kanäle (Concept Test)

| Erlaubt | Nicht erlaubt |
|---|---|
| Meta Link-Ads, Meta Lead Ads | Google Search |
| Pinterest Standard-Pins mit "Noch nicht erhältlich" | Shopping-, Katalog-, Feed-Formate aller Kanäle |
| TikTok In-Feed mit Website-Ziel (mit AIGC-Label) | Amazon/Etsy/Kaufland-Ads |

## Recht und Formulierungen

- Jede Konzeptseite zeigt: Konzeptstatus, Preis inkl. MwSt. above the fold, Hinweis auf Visualisierung.
- KI-generierte oder KI-bearbeitete Produktbilder werden gekennzeichnet (Art. 50 AI Act).
- Keine Frische- oder Wirkversprechen ohne eigenen Test.
- Keine Streichpreise, kein "auf Lager", "jetzt kaufen", "Lieferung in X Tagen".
- Neue Claims oder Formulierungen außerhalb von `playbook/learning.md#freigegebene-formulierungen` gehen immer über Patrick.
- Reservierungsstufe erst nach Anwaltsprüfung (Fernabsatz, Lieferzeitangabe).
- Pixel nur nach Einwilligung. Warteliste mit Double Opt-in.

## Trennung

- Eigener Shopify-Store und eigene Ad-Konten, getrennt von Eshop-Guide- und Kundenkonten.
- Worker bekommt keinen Store-Token mit Publish-Rechten. Seiten kommen als Git-Artefakt.
