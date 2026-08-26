# 🌴 Travel Blog

Eine responsive Multi-Page-Website für einen Reiseblog, umgesetzt in reinem **HTML5** und **CSS3** – ohne JavaScript-Framework, ohne Build-Tools. Der Fokus liegt auf einem konsistenten, wiederverwendbaren Design-System (Farben, Typografie, Spacing) über mehrere Artikeltypen hinweg (Text mit Diagrammen, Bildkarussell, Video).

---

## 📖 Über das Projekt

Der Travel Blog besteht aus einer Startseite mit Hero-, Highlights-, FAQ- und Kontaktbereich sowie mehreren Artikel-Templates, die unterschiedliche redaktionelle Inhaltstypen abdecken: Statistik-Grafiken, Bildergalerien und eingebettete Videos. Header, Footer und mobile Navigation sind seitenübergreifend konsistent.

## ✨ Features

- **Vollständig responsive** – Mobile-first-Ansatz mit Breakpoint bei `768px`
- **Eigenes Design-System** – zentrale Farb-, Spacing- und Typografie-Variablen in `global.css`
- **Self-hosted Webfonts** (`Arima`, `Palanquin`, `Palanquin Dark`) im WOFF2-Format – keine externen Font-Requests
- **Mobile Bottom-Navigation** (fixiert) und **Desktop-Menü**, abhängig vom Breakpoint ein-/ausgeblendet
- **Wiederverwendbare Komponenten**: Autoren-Karte, Meta-Infos (Datum/Lesezeit/Views/Shares), Footer, Share-Bereich
- **Mehrere Artikel-Layouts**: Diagramme, responsives Bildkarussell, HTML5-Video mit Poster-Bild
- **Barrierearme Basics**: `scroll-behavior` respektiert `prefers-reduced-motion`, `alt`-Texte auf allen Bildern, sichtbare Fokus-Zustände auf Links

## 🖥️ Seitenübersicht

| Datei                   | Beschreibung                                                                                                                 |
| ----------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| `index.html`            | Startseite – Hero, Highlights, FAQ, Kontakt                                                                                  |
| `article-graph.html`    | Artikel „The World's Most Breathtaking Beaches" mit Statistik-Diagrammen (Regenzeiten, Strandaktivitäten, Unterkunftskosten) |
| `article-carousel.html` | Artikel „The World's Most Breathtaking Beaches" mit responsivem Bildkarussell                                                |
| `article-video.html`    | Artikel „Copenhagen in 3 Days" mit eingebettetem Video                                                                       |
| `privacy.html`          | Datenschutzerklärung                                                                                                         |

## 🛠️ Tech-Stack

- **HTML5** (semantisches Markup: `header`, `nav`, `section`, `article`-Inhalte, `footer`)
- **CSS3** – Flexbox-Layouts, CSS Custom Properties, `clamp()` für fluid Spacing/Typografie, Media Queries
- Keine JavaScript-Abhängigkeiten, keine Build-Pipeline – rein statische Auslieferung

## 📁 Projektstruktur

```
blog_group_project/
├── index.html
├── article-graph.html
├── article-carousel.html
├── article-video.html
├── privacy.html
├── README.md
└── assets/
    ├── css/
    │   ├── fonts.css              # @font-face Definitionen
    │   ├── global.css             # Reset, Farbvariablen, Header/Footer, Nav
    │   ├── index.css              # Styles für die Startseite
    │   ├── article-graph.css      # Styles für den Diagramm-Artikel
    │   ├── article-carousel.css   # Styles für den Karussell-Artikel
    │   └── article-video.css      # Styles für den Video-Artikel
    ├── fonts/                     # Arima & Palanquin (WOFF2)
    ├── icon/                      # UI-Icons (SVG)
    ├── img/                       # Fotos, Illustrationen, Diagramme
    └── video/                     # Artikel-Video (MP4)
```

## 🎨 Design-Tokens

Zentrale Farbvariablen, definiert in `assets/css/global.css`:

| Variable                     | Wert                      | Verwendung                                                 |
| ---------------------------- | ------------------------- | ---------------------------------------------------------- |
| `--color-primary-green`      | `#4EA487`                 | Header/Footer-Hintergrund, Überschriften, mobile Nav-Icons |
| `--color-primary-yellow`     | `#F1C953`                 | Hero-Hintergrund, mobile Bottom-Nav, Button-Text           |
| `--color-bg-light-green`     | `rgba(78, 164, 135, 0.2)` | Autoren-Karte, Pro-Tipp-Boxen                              |
| `--color-text-main`          | `#3D3D3D`                 | Fließtext                                                  |
| `--color-secondary-brown`    | `#54370D`                 | Meta-Angaben, Autoren-Text                                 |
| `--container-padding-inline` | `clamp(1rem, 5vi, 4rem)`  | Responsiver Außenabstand                                   |

## 📐 Responsive Verhalten

- **`< 768px`**: Mobile Navigation (fixierte Bottom-Bar), Desktop-Menü ausgeblendet, einspaltige Inhalte.
- **`≥ 768px`**: Desktop-Menü im Header sichtbar, mobile Bottom-Bar ausgeblendet, mehrspaltige Content-Bereiche.
- Inhaltsbreiten auf den Artikelseiten ist begrenzt und zentriert; Header und Footer behalten unabhängig davon ihre volle Breite mit Hintergrundfarbe.

## 🚀 Lokal ausführen

Da es sich um eine rein statische Website handelt, reicht ein einfacher lokaler Webserver (nötig, damit relative Asset-Pfade korrekt aufgelöst werden):

```bash
# Im Projektordner:
python3 -m http.server 8000
# Danach im Browser öffnen:
# http://localhost:8000/index.html
```

Alternativ z. B. mit der VS-Code-Erweiterung **Live Server**.

## 🔤 Schriftarten

- **Arima** (Gewichte 400/500/600/700) – Überschriften
- **Palanquin** / **Palanquin Dark** (Gewichte 400/500/600/700) – Fließtext & UI-Elemente

Beide Schriften liegen lokal im WOFF2-Format unter `assets/fonts/` und werden über `assets/css/fonts.css` eingebunden.

## 📄 Lizenz / Hinweis

Dieses Projekt wurde im Rahmen einer Gruppenarbeit erstellt. Platzhalterinhalte (Lorem-Ipsum-Texte, Kontaktformular, Social-Media-Links) dienen ausschließlich Demonstrationszwecken.
