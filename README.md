# Travel Blog – Gruppenprojekt

Statische Multi-Page-Website (reines HTML/CSS, kein Build-Step) für einen Reiseblog.

## Seiten

| Datei | Inhalt |
| --- | --- |
| `index.html` | Startseite mit Hero, Highlights-Slider, FAQ und Kontakt |
| `article-carousel.html` | Artikel „The World's Most Breathtaking Beaches" (Bildergalerie) |
| `article-video.html` | Artikel „Copenhagen in 3 Days" (mit Video) |
| `article-graph.html` | Artikel „Pattaya Pulse / Thailand" (mit Infografik) |
| `privacy.html` | Privacy Policy |

## Lokal ansehen

Einfach `index.html` im Browser öffnen – oder einen kleinen Server starten:

```bash
npx serve .
# oder
python -m http.server 8000
```

## Struktur

```
assets/
  css/     → global.css (Reset + Design-Tokens), fonts.css, je eine CSS-Datei pro Seite
  img/     → Bilder
  icon/    → Icons & Favicon
  video/   → Videos
```

## Arbeitsaufteilung

Die Zuständigkeiten sind per Kommentar in den HTML-Dateien markiert
(z. B. `<!-- SELIM ARBEITET BIS HIER - FINGER WEG -->`). Bitte diese Grenzen respektieren.

## Konventionen

- Design-Tokens (Farben etc.) zentral in `assets/css/global.css` unter `:root` pflegen.
- Dekorative Bilder bekommen `alt=""`, inhaltliche Bilder einen beschreibenden Alt-Text.
- Bilder unterhalb des Viewports mit `loading="lazy"` einbinden.
