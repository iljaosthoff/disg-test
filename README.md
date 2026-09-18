# DISG-Test

Ein kostenloser DISG-Test (international: DISC) mit 28 Aussagen und ausführlicher Auswertung.

**Live:** https://iljaosthoff.github.io/disg-test/

## Was es ist

Eine einzelne statische HTML-Datei ohne Abhängigkeiten, ohne Build-Schritt und ohne Backend.

- 7 Runden à 4 Aussagen, Forced-Choice — aufgeteilt in **14 Schritte mit je einer Entscheidung**: erst „am meisten“, dann „am wenigsten“. Ein Klick pro Schritt, es geht automatisch weiter.
- Auswertung mit Balkendiagramm, Haupt- und Zweitstil, Mischtyp-Deutung
- Pro Stil: Antrieb, Stärken, Stressverhalten, blinder Fleck, Kommunikationshinweise
- Warnt ausdrücklich, wenn die beiden stärksten Stile weniger als zwei Punkte auseinanderliegen — bei diesem Testumfang ist das kein echter Unterschied
- Hell- und Dunkelmodus, Umschalter oben rechts
- Ergebnis teilbar per URL (`#r=...`), kopierbar, druckbar als PDF

## Datenschutz

Alles läuft im Browser. Keine Antworten werden übertragen, keine Cookies gesetzt, keine Daten gespeichert. Einzige Ausnahme: die gewählte Hell-/Dunkel-Einstellung liegt in `localStorage` des jeweiligen Browsers.

## Anpassen

Alles Inhaltliche steht im `<script>`-Block ganz unten in `index.html`:

| Konstante | Inhalt |
|---|---|
| `TYPES` | Texte je Stil (D, I, S, G) |
| `MIX` | Deutungen der Zweier-Kombinationen |
| `BLOCKS` | die 7 Runden mit je 4 Aussagen |

Die Farben sind CSS-Variablen `--d`, `--i`, `--s`, `--g` im `:root`-Block — jeweils einmal für hell und einmal für dunkel.

**Konvention:** Die Datei enthält bewusst **keinen einzigen Backslash** (Regex nutzt `[0-9]` statt `\d`, Zeilenumbrüche kommen aus `String.fromCharCode(10)`). Grund: Beim Hochladen über API-Werkzeuge gingen Escape-Sequenzen schon einmal kaputt. Wer hier editiert, sollte das so lassen.

## Offen

- [x] Impressum-Link im Footer (zeigt auf ilja-osthoff.ch)
- [ ] optional: Call-to-Action am Ende der Auswertung
- [ ] optional: längere Variante mit 12 Runden für feinere Auflösung

## Einordnung

DISG geht auf William Moulton Marston (1928) zurück und beschreibt Verhalten in Situationen, keine Persönlichkeit. Das Modell ist wissenschaftlich deutlich schwächer belegt als etwa die Big Five und ist kein Diagnoseinstrument. Fragen und Auswertungstexte hier sind eine eigenständige Umsetzung und kein Lizenzprodukt.
