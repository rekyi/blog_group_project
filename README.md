# 🌴 Travel Blog

A responsive multi-page website for a travel blog, built with pure **HTML5** and **CSS3** – no JavaScript framework, no build tools. The focus is on a consistent, reusable design system (colors, typography, spacing) across multiple article types (text with charts, image carousel, video).

---

## 📖 About the Project

The Travel Blog consists of a homepage with hero, highlights, FAQ, and contact sections, plus several article templates covering different editorial content types: statistics charts, image galleries, and embedded videos. The header, footer, and mobile navigation stay consistent across all pages.

## ✨ Features

- **Fully responsive** – mobile-first approach with a breakpoint at `768px`
- **Custom design system** – central color, spacing, and typography variables in `global.css`
- **Self-hosted webfonts** (`Arima`, `Palanquin`, `Palanquin Dark`) in WOFF2 format – no external font requests
- **Mobile bottom navigation** (fixed) and **desktop menu**, shown/hidden depending on the breakpoint
- **Reusable components**: author card, meta info (date/reading time/views/shares), footer, share section
- **Multiple article layouts**: charts, responsive image carousel, HTML5 video with poster image
- **Basic accessibility**: `scroll-behavior` respects `prefers-reduced-motion`, `alt` text on all images, visible focus states on links

## 🖥️ Page Overview

| File                    | Description                                                                                                             |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| `index.html`            | Homepage – hero, highlights, FAQ, contact                                                                               |
| `article-graph.html`    | Article "The World's Most Breathtaking Beaches" with statistics charts (rainy seasons, beach activities, lodging costs) |
| `article-carousel.html` | Article "The World's Most Breathtaking Beaches" with a responsive image carousel                                        |
| `article-video.html`    | Article "Copenhagen in 3 Days" with an embedded video                                                                   |
| `privacy.html`          | Privacy policy                                                                                                          |

## 🛠️ Tech Stack

- **HTML5** (semantic markup: `header`, `nav`, `section`, `article` content, `footer`)
- **CSS3** – Flexbox layouts, CSS Custom Properties, `clamp()` for fluid spacing/typography, media queries
- No JavaScript dependencies, no build pipeline – purely static delivery

## 📁 Project Structure

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
    │   ├── fonts.css              # @font-face definitions
    │   ├── global.css             # Reset, color variables, header/footer, nav
    │   ├── index.css              # Styles for the homepage
    │   ├── article-graph.css      # Styles for the chart article
    │   ├── article-carousel.css   # Styles for the carousel article
    │   └── article-video.css      # Styles for the video article
    ├── fonts/                     # Arima & Palanquin (WOFF2)
    ├── icon/                      # UI icons (SVG)
    ├── img/                       # Photos, illustrations, charts
    └── video/                     # Article video (MP4)
```

## 🎨 Design Tokens

Central color variables, defined in `assets/css/global.css`:

| Variable                     | Value                     | Usage                                                |
| ---------------------------- | ------------------------- | ---------------------------------------------------- |
| `--color-primary-green`      | `#4EA487`                 | Header/footer background, headings, mobile nav icons |
| `--color-primary-yellow`     | `#F1C953`                 | Hero background, mobile bottom nav, button text      |
| `--color-bg-light-green`     | `rgba(78, 164, 135, 0.2)` | Author card, pro-tip boxes                           |
| `--color-text-main`          | `#3D3D3D`                 | Body text                                            |
| `--color-secondary-brown`    | `#54370D`                 | Meta info, author text                               |
| `--container-padding-inline` | `clamp(1rem, 5vi, 4rem)`  | Responsive outer padding                             |

## 📐 Responsive Behavior

- **`< 768px`**: Mobile navigation (fixed bottom bar), desktop menu hidden, single-column content.
- **`≥ 768px`**: Desktop menu visible in the header, mobile bottom bar hidden, multi-column content areas.
- Content width on the article pages is constrained and centered; the header and footer keep their full width with background color regardless.

## 🚀 Running Locally

Since this is a purely static website, a simple local web server is enough:

```bash
# In the project folder:
python3 -m http.server 8000
# Then open in your browser:
# http://localhost:8000/index.html
```

Alternatively, e.g. with the VS Code extension **Live Server**.

## 🔤 Fonts

- **Arima** (weights 400/500/600/700) – headings
- **Palanquin** / **Palanquin Dark** (weights 400/500/600/700) – body text & UI elements

Both fonts are hosted locally in WOFF2 format under `assets/fonts/` and are included via `assets/css/fonts.css`.

## 📄 License / Note

This project was created as part of a group assignment. Placeholder content (lorem ipsum text, contact form, social media links) is for demonstration purposes only.
