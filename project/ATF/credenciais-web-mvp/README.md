# ATF Credentials Web

## Overview

This repository contains the HTML implementation, assets, references and documentation for the ATF Credentials presentation.

The original presentation was designed in Figma. After testing Figma Slides and other presentation formats, the team chose an HTML-based approach to preserve the visual quality of the design while adding richer motion, video handling, controlled transitions and browser-based presentation behavior.

The project evolved from a five-slide MVP into a complete 59-slide web presentation with dedicated desktop and mobile versions.

---

## Current Scope

The current version includes the full ATF Credentials presentation:

* 59 slides
* Full 1920 × 1080 presentation canvas
* Desktop version optimized for browser presentation
* Mobile version optimized for horizontal viewing on smartphones
* Keyboard navigation on desktop
* Swipe/tap navigation on mobile
* Image backgrounds
* Animated logo intros
* Animated illustration backgrounds
* Product/interface motion assets
* SVG text highlights
* ATF, ATF Asset and ATF Fintech logo systems
* Final slide with external website and email links

---

## Local / Hosted Usage

This package is environment-agnostic. It can be hosted in any static web environment, as long as the folder structure is preserved and the HTML files can access the relative assets.

### Desktop version

```text
index-desktop.html
```

### Mobile version

```text
index-mobile.html
```

If hosted on a server or CDN, the final URLs should follow the structure defined by the ATF development team. Example:

```text
https://{host}/{path}/index-desktop.html
https://{host}/{path}/index-mobile.html
```

For cache-busting after deploys, append a query parameter such as:

```text
index-desktop.html?v=latest
index-mobile.html?v=latest
```

### Important note

The previous `index.html` entry point was intentionally removed. The current delivery uses separate desktop and mobile HTML files.

---

## Recommended Usage

### Desktop / notebook

Use:

```text
index-desktop.html
```

Recommended environment:

* Chrome, Safari or Edge on desktop
* 16:9 screen or fullscreen browser window
* Keyboard navigation with arrow keys or spacebar

### Mobile

Use:

```text
index-mobile.html
```

Recommended environment:

* Smartphone in horizontal / landscape orientation
* Open directly in browser whenever possible
* Use swipe or tap navigation

The mobile version includes a portrait notice asking the user to rotate the device. The fullscreen button was removed because fullscreen behavior is inconsistent across mobile browsers, especially on iOS/Safari.

---

## Source Material

The project is based on:

* Original Figma design file
* Exported slide references from Figma
* Motion assets developed for ATF
* Animated product mockups
* SVG highlights exported from Figma
* ATF brand assets and logo system
* Slide-by-slide implementation notes documented in the project brief

---

## Folder Structure

```text
credenciais-web-mvp
├── assets
│   ├── images
│   │   ├── slide-2-image-bg.jpg
│   │   ├── slide-3-image-bg.jpg
│   │   ├── ...
│   │   └── slide-52-image-bg.jpg
│   │
│   ├── logos
│   │   ├── logo-atf-asset-black.svg
│   │   ├── logo-atf-asset-white.svg
│   │   ├── logo-atf-black.svg
│   │   ├── logo-atf-fintech-black.svg
│   │   ├── logo-atf-fintech-white.svg
│   │   ├── logo-atf-white.svg
│   │   ├── symbol-atf-black.svg
│   │   └── symbol-atf-white.svg
│   │
│   ├── text-highlight-background
│   │   ├── slide-05-highlight-01.svg
│   │   ├── slide-05-highlight-02.svg
│   │   ├── ...
│   │   └── slide-49-highlight-02.svg
│   │
│   └── videos
│       ├── atf-logo-animation.mp4
│       ├── atf-asset-logo-animation.mp4
│       ├── atf-fintech-logo-animation.mp4
│       ├── slide-7-animation-background.mp4
│       ├── slide-9-animation-background.mp4
│       ├── slide-18-animation-background.mp4
│       ├── slide-33-animation-background.mp4
│       ├── slide-34-animation-background.mp4
│       ├── slide-35-animation-background.mp4
│       ├── slide-36-animation-background.mp4
│       ├── slide_40-motion-conta-pj.mp4
│       ├── slide_41-motion-seguranca.mp4
│       ├── slide_42-motion-internet-banking.mp4
│       ├── slide_43-motion-app-atf.mp4
│       ├── slide_44-motion-pix-empresarial.mp4
│       ├── slide_45-motion-boleto.mp4
│       └── slide_46-motion-pagamentos.mp4
│
├── references
│   ├── slide_01.jpg
│   ├── slide_02.jpg
│   ├── ...
│   └── slide_52.jpg
│
├── slides
│   └── slides-full-brief.md
│
├── index-desktop.html
├── index-mobile.html
└── README.md
```

---

## Key Documents

### `slides/slides-full-brief.md`

Primary implementation brief.

Contains:

* Canvas setup
* Grid system
* Typography system
* Asset naming conventions
* Background maps
* Logo maps
* Highlight maps
* Video maps
* Slide-by-slide content
* Animation behavior
* Presentation requirements

This file should be treated as the source of truth for future visual and structural updates.

### `index-desktop.html`

Desktop presentation file.

Contains:

* Full slide markup
* Embedded CSS
* Animation rules
* Keyboard navigation
* Desktop-oriented video handling
* Final contact links

### `index-mobile.html`

Mobile presentation file.

Contains:

* Mobile-optimized slide rendering
* Embedded CSS
* Portrait rotate notice
* Swipe and tap navigation
* Dynamic media handling with lazy loading
* iOS-oriented video and image release behavior
* Final contact links

---

## Design System

### Canvas

```text
Width: 1920px
Height: 1080px
Aspect Ratio: 16:9
```

### Grid

```text
Columns: 16
Rows: 11
Margin: 64px
Gutter: 32px
Type: Stretch
```

### Typography

Primary typeface:

```text
Plus Jakarta Sans
```

Type scale:

| Figma Name | CSS Class | Weight | Size | Line Height | Letter Spacing |
|---|---|---:|---:|---:|---:|
| TEXTO_PPP | `text-caption` | 700 | 21px | 120% | -1% |
| TEXTO_PP | `text-body-large` | 600 | 48px | 55px | -1% |
| TEXTO_P | `text-statement-small` | 700 | 64px | 110% | -1% |
| TEXTO_M | `text-statement-medium` | 700 | 73px | 80px | -1% |
| TEXTO_G | `text-statement-large` | 700 | 96px | 100% | -1% |
| TEXTO_GG | `text-display-medium` | 700 | 108px | 110% | -1% |
| TEXTO_GGG | `text-display-large` | 500 | 164px | 140px | -1% |

Some slides include manual line locking for Figma fidelity, especially when browser text wrapping differs from Figma rendering.

---

## Asset Naming Conventions

### Slide References

```text
references/slide_01.jpg
references/slide_02.jpg
...
references/slide_52.jpg
```

### Image Backgrounds

```text
assets/images/slide-{number}-image-bg.jpg
```

Example:

```text
assets/images/slide-24-image-bg.jpg
```

Slides with image background:

```text
02, 03, 04, 08, 10, 11, 13, 15, 17, 24, 25, 27, 29, 31,
39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 50, 51, 52
```

### Animated Illustration Backgrounds

```text
assets/videos/slide-{number}-animation-background.mp4
```

Slides with animated illustration background:

```text
07, 09, 18, 33, 34, 35, 36
```

### Brand Logo Animation Videos

```text
assets/videos/atf-logo-animation.mp4
assets/videos/atf-asset-logo-animation.mp4
assets/videos/atf-fintech-logo-animation.mp4
```

Usage:

```text
Slide 01 — ATF logo animation
Slide 23 — ATF Asset logo animation
Slide 37 — ATF Fintech logo animation
```

### Product Motion Videos

```text
assets/videos/slide_40-motion-conta-pj.mp4
assets/videos/slide_41-motion-seguranca.mp4
assets/videos/slide_42-motion-internet-banking.mp4
assets/videos/slide_43-motion-app-atf.mp4
assets/videos/slide_44-motion-pix-empresarial.mp4
assets/videos/slide_45-motion-boleto.mp4
assets/videos/slide_46-motion-pagamentos.mp4
```

Usage:

```text
Slide 41 — Conta PJ
Slide 43 — Segurança
Slide 45 — Internet Banking
Slide 47 — App ATF
Slide 49 — Pix Empresarial
Slide 51 — Boleto Bancário
Slide 53 — Pagamentos
```

### Text Highlight Backgrounds

Text highlights are exported as individual SVG files per slide and per occurrence.

```text
assets/text-highlight-background/slide-05-highlight-01.svg
assets/text-highlight-background/slide-05-highlight-02.svg
...
assets/text-highlight-background/slide-49-highlight-02.svg
```

This approach is used instead of a single master SVG because each highlight requires precise Figma fidelity.

---

## Slide Architecture

### Opening

| Slide | Description |
|---:|---|
| 01 | ATF animated logo intro |
| 02 | Brand hero: “Fintech para negócios” |
| 03–04 | Institutional manifesto |
| 05–22 | ATF positioning, values, credibility and architecture |

### Asset Section

| Slide | Description |
|---:|---|
| 23 | ATF Asset animated logo intro |
| 24–32 | Asset positioning, FIDC and credit structure |
| 33–36 | Credit product slides with animated illustration backgrounds |

### Fintech Section

| Slide | Description |
|---:|---|
| 37 | ATF Fintech animated logo intro |
| 38–39 | Fintech platform positioning |
| 40–53 | Fintech product and interface motion sequence |
| 54–56 | Service, infrastructure and technology positioning |

### Closing

| Slide | Description |
|---:|---|
| 57 | Final positioning statement |
| 58 | “Confie no futuro.” |
| 59 | Final contact slide with website, email and phone |

---

## Logo System

### Standard ATF Symbol

Default size and position:

```text
Width: 64.84px
Height: 28.2px
X: 64px
Y: 988px
```

Used in black or white depending on background contrast.

### ATF Asset Footer Logo

Default size and position:

```text
Width: 266.52px
Height: 28.2px
X: 64px
Y: 988px
```

### ATF Fintech Footer Logo

Default size and position:

```text
Width: 310.96px
Height: 28.2px
X: 64px
Y: 988px
```

### Final Slide Symbol

Slide 59 uses a special ATF symbol size and position:

```text
Width: 279.11px
Height: 121.39px
X: 64px
Y: 479px
```

---

## Presentation Behavior

### Desktop

The desktop version is optimized for browser-based presentation use.

Keyboard controls:

```text
Arrow Right / Space — Next slide
Arrow Left — Previous slide
```

Videos:

* Play when the slide becomes active
* Restart from the beginning on slide entry
* Remain muted
* Use `playsinline`
* Logo intro videos loop
* Background illustration videos are used as full-canvas visual layers
* Product motion videos are used in the Fintech product sequence

Navigation UI:

* No visible navigation indicator in the final version

### Mobile

The mobile version keeps the same 16:9 presentation experience while adapting the technical behavior for smartphone browsers.

Mobile controls:

```text
Swipe left — Next slide
Swipe right — Previous slide
Tap right side — Next slide
Tap left side — Previous slide
```

Mobile behavior:

* Designed for landscape orientation
* Portrait mode displays a rotate-device notice
* Fullscreen button removed
* Slides are rendered dynamically
* Media assets are loaded only when needed
* Videos and images are released when a slide is removed
* Optimized to reduce iOS/Safari memory issues

---

## Final Slide Links

Slide 59 includes:

```text
https://atf.com.br
mailto:falecom@atf.com.br
0800 888 5151
```

---

## Deploy Workflow

This package does not depend on a specific repository, domain or hosting provider.

To deploy:

1. Upload the complete `credenciais-web-mvp` folder to the desired static hosting environment.
2. Preserve the internal folder structure.
3. Confirm that both HTML files can access the relative asset paths.
4. Test the desktop and mobile entry points.
5. Use cache-busting query parameters after updates if needed.

Entry points:

```text
index-desktop.html
index-mobile.html
```

If using Git, commit the full folder or the specific changed files according to the team's deployment workflow.

Example:

```bash
git status
git add path/to/credenciais-web-mvp
git commit -m "Update ATF credentials presentation"
git push
```

If the live site does not update immediately:

1. Check the hosting/deploy status.
2. Open the URL with a cache-busting query parameter.
3. Hard refresh the browser.
4. Test in an incognito/private window.

---

## Packaging / Client Handoff

When preparing a ZIP for client handoff, include the complete `credenciais-web-mvp` folder with:

```text
assets/
references/
slides/
index-desktop.html
index-mobile.html
README.md
```

Do not rename or move files inside `assets`, because the HTML files use relative paths.

Recommended package name:

```text
ATF-Credentials-Web-Final.zip
```

Recommended hosted links should be defined by the ATF development team after installation in the final environment.

Suggested public routes:

```text
Desktop:
https://{host}/{path}/index-desktop.html

Mobile:
https://{host}/{path}/index-mobile.html
```

---

### Environment note

Any staging URLs used during development are not required for the final installation and should not be treated as production dependencies.

---

## Technical Notes

* The project is implemented as a self-contained HTML presentation with external relative assets.
* CSS is embedded in each HTML file.
* Assets are loaded through relative paths.
* The desktop version prioritizes the approved presentation experience.
* The mobile version prioritizes stability and media handling on smartphone browsers.
* Figma fidelity sometimes requires manual line breaks or locked line spans.
* Highlights use slide-specific SVG files for better rendering accuracy.
* Mobile fullscreen was intentionally removed due to inconsistent support across mobile browsers.

---

## Status

Current phase:

```text
Final client handoff
```

Slides included:

```text
01–59
```

Latest updates:

* Desktop and mobile versions separated
* Full 59-slide presentation assembled
* Product motion sequence added to the Fintech section
* App ATF motion video updated
* Slide-specific highlights implemented
* Typography and line-break fixes applied
* Mobile dynamic rendering implemented
* Mobile fullscreen button removed
* Final slide links added

Next step:

```text
Package ZIP, share live links and hand off files to the client / DevOps team.
```

---

## Long-Term Vision

This project is more than a one-off HTML version of the ATF Credentials presentation.

It establishes a reusable presentation framework for high-end institutional narratives, capable of combining:

* Editorial layouts
* Brand systems
* Motion graphics
* Product videos
* SVG highlights
* Image backgrounds
* Interactive navigation
* Future updates with controlled visual fidelity

The framework can be adapted for future ATF materials and other institutional presentations.
