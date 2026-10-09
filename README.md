# Justin Phoo Hoe Yin · Portfolio

Personal portfolio of **Justin Phoo Hoe Yin**, an upcoming Bachelor of Information Technology (Honours) graduate specialising in Business Intelligence and Analytics.

**Live site:** https://nitseyj.github.io/portfolio/

The site is a single static page with no build step. All markup, styles and scripts live in `index.html`.

---

## Contents

- [Sections](#sections)
- [Interactive features](#interactive-features)
- [Tech stack](#tech-stack)
- [Design system](#design-system)
- [Accessibility and performance](#accessibility-and-performance)
- [Project structure](#project-structure)
- [Running locally](#running-locally)
- [Deployment](#deployment)
- [Editing content](#editing-content)
- [Contact](#contact)

---

## Sections

| Section | Purpose |
| --- | --- |
| **Hero** | Name, field, location and email, followed by the headline, a short introduction and links to work, LinkedIn and GitHub. |
| **Approach** | A one-line summary of the portfolio, shown beside a rotating data-point globe. |
| **Things I've built** | Bento grid with a playable anomaly-spotting chart and cards for BI reporting, pipelines and AI-built tools. |
| **Featured projects** | Four stacked project cards: Retail ELT pipeline, Anomaly Hunt, Valorant Analyst and WWMG. |
| **Skills & tools** | Expandable panels covering BI, programming, databases, development, AI and languages, each linked to the projects that use them. |
| **Background** | Education timeline and certifications. |
| **Contact** | Availability for roles and collaborations, with email, LinkedIn and GitHub. |

## Interactive features

- **Spot the anomaly:** a mini version of the Anomaly Hunt game. Each series contains one injected outlier, and the game tracks your streak and best score.
- **Rotating data globe:** a canvas-rendered sphere of data points with highlighted "signal" points.
- **Animated hero background:** a canvas wave field behind the headline.
- **Stacked project cards:** cards pin and stack while scrolling, with a project index and counter alongside.
- **Skills accordion:** opens on hover or click on desktop and stacks on mobile.
- **One-click email copy:** in both the hero and the contact section.
- **Theme toggle:** cycles through auto, light and dark modes and remembers your choice.
- **Motion toggle:** pauses every looping animation (marquees, canvases, typing terminal) and remembers your choice.
- **Scroll choreography:** word-by-word text reveals, smooth scrolling and a reading-progress bar.

## Tech stack

| Area | Tools |
| --- | --- |
| Markup and styling | HTML5, modern CSS (custom properties, grid, `clamp()`, `color-scheme`) |
| Scripting | Vanilla JavaScript, Canvas 2D |
| Animation | [GSAP 3](https://gsap.com/) with ScrollTrigger, [Lenis](https://lenis.darkroom.engineering/) for smooth scrolling |
| Fonts | [Newsreader](https://fonts.google.com/specimen/Newsreader), [Hanken Grotesk](https://fonts.google.com/specimen/Hanken+Grotesk) and [Geist Mono](https://fonts.google.com/specimen/Geist+Mono), loaded from Google Fonts |
| Hosting | GitHub Pages |

Third-party libraries load from public CDNs (cdnjs and jsDelivr). There are no npm dependencies.

## Design system

- **Concept:** "signal in the noise." A single accent colour marks the signal everywhere: the flagged anomaly, the active state and the call to action. Everything else uses one cool neutral family.
- **Colour tokens:** defined as CSS custom properties on `:root`, with separate light and dark values.

  | Token | Light | Dark |
  | --- | --- | --- |
  | `--bg` | `#eef1f3` | `#0a0d12` |
  | `--ink` | `#0d1117` | `#eef2f6` |
  | `--muted` | `#38414c` | `#b6c0cc` |
  | `--accent` | `#3f6b00` | `#c8f169` |

- **Typography:** Newsreader (serif) for headings, Hanken Grotesk for body text, and Geist Mono for labels and data.

## Accessibility and performance

- Respects `prefers-reduced-motion`: animations are disabled and canvases render a still frame.
- Respects `prefers-color-scheme`, with a manual override.
- Skip-to-content link, visible focus rings, semantic landmarks and ARIA labels on interactive controls.
- Muted text is tuned for readable contrast in both themes.
- A motion toggle in the nav pauses all looping animation (WCAG 2.2.2).
- The mobile menu keeps keyboard focus inside it while open; copy actions are announced to screen readers.
- Canvas animations pause when off-screen. Scroll effects animate only `transform` and `opacity`.
- Fully responsive, from 360px phones to wide desktop screens.

## Project structure

```
portfolio/
├── index.html     # The entire site: markup, styles and scripts
├── og-image.png   # 1200×630 link-preview card for LinkedIn and other sites
└── README.md      # This file
```

## Running locally

No installation or build step is needed.

1. Clone the repository:
   ```bash
   git clone https://github.com/nitseyj/portfolio.git
   cd portfolio
   ```
2. Open `index.html` in a browser, or serve the folder with a local server such as the VS Code **Live Server** extension.

An internet connection is required for fonts and animation libraries, which load from CDNs.

## Deployment

The site deploys automatically through **GitHub Pages**:

- **Source:** `main` branch, repository root (`/`).
- **Updates:** push to `main`. Changes go live within a minute or two.
- If changes don't appear, hard-refresh the browser with `Ctrl + F5`.

## Editing content

All content lives in `index.html`:

| To change | Look for |
| --- | --- |
| Name, tags and introduction | `<header class="hero">` |
| Projects | `<article class="pcard">` blocks inside `#work` |
| Skills | `.panel` blocks inside `#acc` |
| Education and certifications | `#background` |
| Colours and fonts | `:root` custom properties at the top of the `<style>` block |

## Contact

- **Email:** justinhyphoo@gmail.com
- **LinkedIn:** [linkedin.com/in/justinphoo](https://www.linkedin.com/in/justinphoo/)
- **GitHub:** [github.com/nitseyj](https://github.com/nitseyj)

---

© 2026 Justin Phoo Hoe Yin. All rights reserved.
