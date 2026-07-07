# ATF Credentials Web

## Overview

This repository contains the HTML implementation, assets, references and documentation for the ATF Credentials presentation.

The original presentation was designed in Figma. After testing Figma Slides and other presentation formats, the team chose an HTML-based approach to preserve the visual quality of the design while adding richer motion, video handling, controlled transitions and fullscreen presentation behavior.

The project has evolved from a five-slide MVP into a complete 52-slide web presentation.

---

## Current Scope

The current version includes the full ATF Credentials presentation:

* 52 slides
* Fullscreen 1920 × 1080 presentation canvas
* Keyboard navigation
* Image backgrounds
* Animated logo intros
* Animated illustration backgrounds
* Product/interface motion assets
* SVG text highlights
* ATF, ATF Asset and ATF Fintech logo systems
* Final slide with external website and email links

---

## Live URL

The presentation is published through GitHub Pages at:

```text
https://paladino.inc/project/ATF/credenciais-web-mvp/index.html
```

For cache-busting after deploys, use:

```text
https://paladino.inc/project/ATF/credenciais-web-mvp/index.html?v=latest
```

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
│       ├── atf-motion-slide-43-conta-pj.mp4
│       ├── slide-7-animation-background.mp4
│       ├── slide-9-animation-background.mp4
│       ├── slide-18-animation-background.mp4
│       ├── slide-33-animation-background.mp4
│       ├── slide-34-animation-background.mp4
│       ├── slide-35-animation-background.mp4
│       └── slide-36-animation-background.mp4
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
├── index.html
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

This file should be treated as the source of truth for future updates.

### `index.html`

Main presentation file.

Contains:

* Full slide markup
* Embedded CSS
* Animation rules
* Keyboard navigation
* Video handling
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
| 38–49 | Fintech platform, product and infrastructure narrative |

### Closing

| Slide | Description |
|---:|---|
| 50 | Final positioning statement |
| 51 | “Confie no futuro.” |
| 52 | Final contact slide with website and email links |

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

Slide 52 uses a special ATF symbol size and position:

```text
Width: 279.11px
Height: 121.39px
X: 64px
Y: 479px
```

---

## Presentation Behavior

The presentation is optimized for desktop fullscreen use.

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
* Logo intro videos play once
* Background illustration videos are used as full-canvas visual layers

Navigation UI:

* No visible navigation indicator in the final version

---

## Final Slide Links

Slide 52 includes:

```text
https://atf.com.br
mailto:falecom@atf.com.br
```

---

## Deploy Workflow

From the local repository:

```bash
git status
git add project/ATF/credenciais-web-mvp
git commit -m "Update ATF credentials HTML presentation"
git push origin main
```

Published URL:

```text
https://paladino.inc/project/ATF/credenciais-web-mvp/index.html
```

If the live site does not update immediately:

1. Check GitHub Actions / Pages deploy status.
2. Open the URL with a cache-busting query parameter.
3. Hard refresh the browser.
4. Test in an incognito window.

---

## Technical Notes

* The project is implemented as a self-contained HTML presentation.
* CSS is embedded in `index.html`.
* Assets are loaded through relative paths.
* The current version is not responsive beyond proportional canvas scaling.
* The target environment is desktop presentation mode.
* Figma fidelity sometimes requires manual line breaks or locked line spans.
* Highlights use slide-specific SVG files for better rendering accuracy.

---

## Status

Current phase:

```text
Full HTML Presentation — Final Review
```

Slides included:

```text
01–52
```

Latest updates:

* Full presentation assembled
* Slide-specific highlights implemented
* Typography and line-break fixes applied
* Slides 12 and 19 line locking corrected
* Navigation indicator removed
* Final slide links added

Next step:

```text
Final QA, GitHub deploy and client review.
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
