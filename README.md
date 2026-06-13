# Elinor — Portfolio Website

Eine voll responsive Onepager-Website, nachgebaut nach der PDF-Vorlage
(`Kopie_Portfolio_onepager_Test2`). Die Seite übernimmt Inhalte, Struktur,
Farbwelt (Palucca-Lime) und die **Originalschriften** aus der Vorlage, ist
aber als eigenständiges, modernes Webdesign mit viel Weißraum umgesetzt –
ähnlich, aber nicht identisch.

## Aufbau / Ansatz

Die Seite ist ein **koordinatengetreuer Nachbau**: Texte, Schriftgrößen,
Farben, Vektorflächen und Bildpositionen wurden direkt aus der PDF ausgelesen
und 1:1 platziert. Alles ist als echtes HTML mit den Originalschriften umgesetzt
und skaliert proportional mit der Breite (CSS `cqw`-Einheiten + `container-type`),
ist also voll responsiv.

```
index.html        – die komplette Seite (beide PDF-Seiten als „Bühnen")
css/
  fonts.css       – @font-face-Einbindung der Originalschriften
  stage.css       – maßstabsgetreues Layout, Effekte
fonts/            – Originalschriften als WOFF2 (aus den .otf/.ttc konvertiert)
assets/           – aus der PDF extrahierte Bilder (mit Transparenz)
```

## Schriften (aus der Vorlage)

- **Helvetica Neue** (Thin – Bold) – Überschriften & Fließtext
- **Helvetica** – ergänzend
- **Minion Pro** – Serifen-Akzente
- **Curt Bloch Block Rough** – handschriftliche Notizen / Marker-Optik

Die `.ttc`-Sammlungen und `.otf`-Dateien wurden für den Web-Einsatz nach
WOFF2 konvertiert (via `fonttools`).

## Lokal ansehen

```bash
python3 -m http.server 8000
# dann http://localhost:8000 öffnen
```

## Hinweise

- Bilder wurden direkt aus der PDF extrahiert (inkl. Soft-Masks/Transparenz).
- Flächige Bilder ohne Transparenz sind als JPEG gespeichert, freigestellte
  Motive als PNG.
- Die Platzhaltertexte (Blindtext) stammen aus der Vorlage.
