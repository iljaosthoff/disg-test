# DISG-Test

Ein kostenloser DISG-Test (international: DISC) mit 28 Aussagen und ausführlicher Auswertung.

**Live:** https://iljaosthoff.github.io/disg-test/

## Was es ist

Eine einzelne statische HTML-Datei ohne Abhängigkeiten, ohne Build-Schritt und ohne Backend.

- 7 Blöcke à 4 Aussagen im Forced-Choice-Format („am meisten“ / „am wenigsten“)
- Auswertung mit Balkendiagramm, Haupt- und Zweitstil, Mischtyp-Deutung
- Pro Stil: Antrieb, Stärken, Stressverhalten, blinder Fleck, Kommunikationshinweise
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
| `BLOCKS` | die 7 Frageblöcke mit je 4 Aussagen |

Die Farben sind CSS-Variablen `--d`, `--i`, `--s`, `--g` im `:root`-Block — jeweils einmal für hell und einmal für dunkel.

## Offen

- [ ] Impressum-Link im Footer setzen (Platzhalter, in DE nach § 5 DDG Pflicht)
- [ ] optional: Call-to-Action am Ende der Auswertung

## Einordnung

DISG geht auf William Moulton Marston (1928) zurück und beschreibt Verhalten in Situationen, keine Persönlichkeit. Das Modell ist wissenschaftlich deutlich schwächer belegt als etwa die Big Five und ist kein Diagnoseinstrument. Fragen und Auswertungstexte hier sind eine eigenständige Umsetzung und kein Lizenzprodukt.
