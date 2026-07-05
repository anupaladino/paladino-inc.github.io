# ATF Credentials HTML Presentation

Version 2.0

---

# Project Overview

This document defines the structure, assets, typography, layout system, animation direction and slide-by-slide content required to build the complete HTML-based version of the ATF Credentials presentation.

The initial MVP validated the migration of the Figma presentation into HTML with high visual fidelity, keyboard navigation, motion support and premium transitions. Version 2.0 expands the brief from the first 5 slides to the full 52-slide production framework.

The goal is no longer only to recreate individual slides. The goal is to build a reusable presentation system for ATF credentials, combining editorial layouts, full-bleed imagery, animated illustrations, brand logo animations, product motion assets and reusable visual components.

---

# Current Folder Structure

```text
atf-credenciais-web
├── assets
│   ├── images
│   │   ├── slide-2-image-bg.jpg
│   │   ├── slide-3-image-bg.jpg
│   │   ├── slide-4-image-bg.jpg
│   │   ├── slide-8-image-bg.jpg
│   │   └── ...
│   │
│   ├── illustrations
│   │   └── [static SVG illustrations, when needed]
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
│   │   └── text-highlight-bg.svg
│   │
│   └── videos
│       ├── atf-logo-animation.mp4
│       ├── atf-asset-logo-animation.mp4
│       ├── atf-fintech-logo-animation.mp4
│       ├── atf-motion-slide-43-conta-pj.mp4
│       ├── slide-7-animation-background.mp4
│       ├── slide-9-animation-background.mp4
│       └── ...
│
├── references
│   ├── slide_01.jpg
│   ├── slide_02.jpg
│   ├── slide_03.jpg
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

# Objectives

The HTML presentation should:

* Preserve the visual quality of the Figma design.
* Support videos and motion assets.
* Support richer animations and transitions than Figma Slides.
* Allow fullscreen presentation mode.
* Be optimized for desktop presentations at 1920x1080.
* Use reusable slide components instead of building every slide as a one-off.
* Become the foundation for future ATF and PALADINO institutional presentations.

---

# Global Setup

## Canvas

Width: 1920px  
Height: 1080px  
Aspect Ratio: 16:9

---

## Layout Grid

Columns: 16  
Rows: 11  
Margin: 64px  
Gutter: 32px  
Type: Stretch

---

# Typography

All type uses Plus Jakarta Sans.

## Type System

| Figma Style | HTML/CSS Class | Weight | Size | Line Height | Letter Spacing | Usage |
|---|---:|---:|---:|---:|---:|---|
| TEXTO_PPP | `text-caption` | 700 | 21px | 120% | -1% | Labels, small notes, auxiliary text |
| TEXTO_PP | `text-body-large` | 600 | 48px | 55px | -1% | Paragraphs, side descriptions, explanatory text |
| TEXTO_P | `text-statement-small` | 700 | 64px | 110% | -1% | Strong subtitles, smaller impact statements |
| TEXTO_M | `text-statement-medium` | 700 | 73px | 80% | -1% | Medium editorial statements |
| TEXTO_G | `text-statement-large` | 700 | 96px | 100% | -1% | Large titles and institutional statements |
| TEXTO_GG | `text-display-medium` | 700 | 108px | 110% | -1% | Main institutional statements |
| TEXTO_GGG | `text-display-large` | 500 | 164px | 140px | -1% | Maximum hero statements |

## CSS Reference

```css
:root {
  --font-primary: "Plus Jakarta Sans", sans-serif;
}

.text-caption {
  font-family: var(--font-primary);
  font-weight: 700;
  font-size: 21px;
  line-height: 120%;
  letter-spacing: -0.01em;
}

.text-body-large {
  font-family: var(--font-primary);
  font-weight: 600;
  font-size: 48px;
  line-height: 55px;
  letter-spacing: -0.01em;
}

.text-statement-small {
  font-family: var(--font-primary);
  font-weight: 700;
  font-size: 64px;
  line-height: 110%;
  letter-spacing: -0.01em;
}

.text-statement-medium {
  font-family: var(--font-primary);
  font-weight: 700;
  font-size: 73px;
  line-height: 80%;
  letter-spacing: -0.01em;
}

.text-statement-large {
  font-family: var(--font-primary);
  font-weight: 700;
  font-size: 96px;
  line-height: 100%;
  letter-spacing: -0.01em;
}

.text-display-medium {
  font-family: var(--font-primary);
  font-weight: 700;
  font-size: 108px;
  line-height: 110%;
  letter-spacing: -0.01em;
}

.text-display-large {
  font-family: var(--font-primary);
  font-weight: 500;
  font-size: 164px;
  line-height: 140px;
  letter-spacing: -0.01em;
}
```

---

# Colors

## White

#FFFFFF

## Black

#000000

## Highlight Gold

Use the exported Figma SVG asset:

```text
assets/text-highlight-background/text-highlight-bg.svg
```

---

# Asset Naming Conventions

## References

All slide reference images use this convention:

```text
references/slide_01.jpg
references/slide_02.jpg
references/slide_03.jpg
...
references/slide_52.jpg
```

## Image Backgrounds

All full-bleed image backgrounds use this convention:

```text
assets/images/slide-{number}-image-bg.jpg
```

Example:

```text
assets/images/slide-8-image-bg.jpg
```

## Animated Illustration Backgrounds

Animated illustration videos use this convention:

```text
assets/videos/slide-{number}-animation-background.mp4
```

Example:

```text
assets/videos/slide-7-animation-background.mp4
```

## Brand Logo Animation Videos

```text
assets/videos/atf-logo-animation.mp4
assets/videos/atf-asset-logo-animation.mp4
assets/videos/atf-fintech-logo-animation.mp4
```

## Product Motion Videos

```text
assets/videos/atf-motion-slide-43-conta-pj.mp4
```

---

# Background System

## Slides with Image Background

Slides with full-bleed JPG background:

```js
const slidesWithImageBackground = [
  2, 3, 4, 8, 10, 11, 13, 15, 17, 24, 25, 27, 29, 31,
  39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 50, 51, 52
];
```

Naming convention:

```text
assets/images/slide-{number}-image-bg.jpg
```

## Slides with Animated Illustration Background

These slides have a white base and a full-canvas MP4 exported at 1920x1080, with the illustration already positioned according to the Figma layout.

```js
const slidesWithAnimatedIllustrationBackground = [7, 9, 18, 33, 34, 35, 36];
```

Naming convention:

```text
assets/videos/slide-{number}-animation-background.mp4
```

Implementation rule:

```text
background: #FFFFFF
video: full canvas 1920x1080
object-fit: cover
muted
playsinline
```

Loop behavior should be defined during polish. Default recommendation: loop subtly for animated illustration backgrounds unless the motion has a clear beginning/end that should play once.

## Brand Logo Animation Slides

These slides use full-canvas logo animation videos.

```js
const brandIntroMap = {
  1: "atf-logo-animation.mp4",
  23: "atf-asset-logo-animation.mp4",
  37: "atf-fintech-logo-animation.mp4"
};
```

Behavior:

* Autoplay when slide becomes active.
* Play once.
* Do not loop.
* Remain on final frame after playback.

## Product Motion Slides

Current validated product motion slide:

```js
const productMotionMap = {
  43: "atf-motion-slide-43-conta-pj.mp4"
};
```

Slide 43 uses the same overlay typography and logo position as Slide 42. The transition from Slide 42 to Slide 43 should feel almost imperceptible: only the background should change from static image to video. Text and logo should not re-enter.

---

# Logo and Symbol System

## Standard ATF Symbol

Assets:

```text
assets/logos/symbol-atf-black.svg
assets/logos/symbol-atf-white.svg
```

Default size and position:

```text
Width: 64.84
Height: 28.2
X: 64
Y: 988
```

Slides with white symbol:

```js
const whiteSymbolSlides = [3, 4, 8, 10, 11, 13, 15, 17, 50];
```

Slides with black symbol:

```js
const blackSymbolSlides = [5, 6, 7, 9, 12, 14, 16, 18, 19, 20];
```

## Special ATF Symbol — Slide 52

```js
const specialSymbolMap = {
  52: {
    src: "assets/logos/symbol-atf-white.svg",
    width: 279.11,
    height: 121.39,
    x: 64,
    y: 479
  }
};
```

## Large Section Logos — Slides 21 and 22

```js
const sectionLogoMap = {
  21: {
    src: "assets/logos/logo-atf-asset-black.svg",
    width: 701.24,
    height: 74,
    x: 64,
    y: 226
  },
  22: {
    src: "assets/logos/logo-atf-fintech-black.svg",
    width: 814.2,
    height: 74,
    x: 64,
    y: 226
  }
};
```

## ATF Asset Footer Logo

Assets:

```text
assets/logos/logo-atf-asset-black.svg
assets/logos/logo-atf-asset-white.svg
```

Default size and position:

```text
Width: 266.52
Height: 28.2
X: 64
Y: 988
```

Slides with black Asset logo:

```js
const blackAssetLogoSlides = [26, 28, 30, 32, 33, 34, 35, 36];
```

Slides with white Asset logo:

```js
const whiteAssetLogoSlides = [24, 25, 27, 29, 31];
```

## ATF Fintech Footer Logo

Assets:

```text
assets/logos/logo-atf-fintech-black.svg
assets/logos/logo-atf-fintech-white.svg
```

Default size and position:

```text
Width: 310.96
Height: 28.2
X: 64
Y: 988
```

Slides with black Fintech logo:

```js
const blackFintechLogoSlides = [38, 49];
```

Slides with white Fintech logo:

```js
const whiteFintechLogoSlides = [39, 40, 41, 42, 43, 44, 45, 46, 47, 48];
```

---

# Text Highlight Background Map

Use one master SVG file for all highlights:

```text
assets/text-highlight-background/text-highlight-bg.svg
```

Implementation rule:

* Position and size are defined per slide.
* The same SVG is reused everywhere.
* Highlight should sit behind the text layer.
* Default `z-index`: highlight below text, above background.
* Recommended animation: horizontal reveal using `scaleX`, with `transform-origin: left center`.

```js
const highlightMap = {
  5: [
    { width: 1067, height: 110, x: 716, y: 610 },
    { width: 899, height: 110, x: 50, y: 719 }
  ],
  6: [
    { width: 660, height: 110, x: 876, y: 332 },
    { width: 361, height: 110, x: 55, y: 442 }
  ],
  7: [
    { width: 902, height: 80, x: 54, y: 546 }
  ],
  9: [
    { width: 464, height: 80, x: 508, y: 469 },
    { width: 315, height: 80, x: 61, y: 548 }
  ],
  12: [
    { width: 1179, height: 100, x: 607, y: 823 }
  ],
  14: [
    { width: 456, height: 100, x: 49, y: 629 }
  ],
  16: [
    { width: 878, height: 100, x: 54, y: 433 }
  ],
  18: [
    { width: 562, height: 110, x: 549, y: 551 },
    { width: 880, height: 110, x: 51, y: 661 }
  ],
  19: [
    { width: 884, height: 110, x: 874, y: 714 },
    { width: 1004, height: 110, x: 51, y: 824 }
  ],
  20: [
    { width: 610, height: 110, x: 863, y: 443 }
  ],
  26: [
    { width: 952, height: 110, x: 52, y: 609 }
  ],
  28: [
    { width: 808, height: 110, x: 301, y: 168 },
    { width: 1327, height: 110, x: 54, y: 718 }
  ],
  30: [
    { width: 1668, height: 110, x: 56, y: 442 }
  ],
  32: [
    { width: 1182, height: 110, x: 670, y: 774 }
  ],
  38: [
    { width: 1589, height: 110, x: 56, y: 498 }
  ],
  49: [
    { width: 418, height: 110, x: 1108, y: 388 },
    { width: 1139, height: 110, x: 64, y: 498 }
  ]
};
```

---

# Animation Direction

## General Slide Transition

Default:

* Fade between slides.
* Avoid heavy motion between consecutive slides with the same layout.
* Keep transitions premium, slow enough to feel deliberate, but not theatrical.

## Text Animation

Default text entrance:

* Fade in.
* Rise 16–20px.
* Duration: 650–850ms.
* Easing: `cubic-bezier(0.22, 1, 0.36, 1)`.

Exception:

* When two consecutive slides share the same text/logo overlay and only background changes, avoid text re-entry.
* Slide 42 → Slide 43 is the current validated example.

## Highlight Animation

Default:

* Reveal horizontally using `scaleX`.
* Transform origin: left center.
* Duration: 650ms.
* Delay after text entrance: 150–300ms.

## Video Behavior

Brand intro videos:

* Play once.
* Do not loop.
* Hold final frame.

Animated illustration backgrounds:

* Autoplay when slide becomes active.
* Muted.
* Plays inline.
* Loop behavior to be defined slide-by-slide during polish.

Product motion videos:

* Autoplay when slide becomes active.
* Muted.
* Plays inline.
* Usually loop if used as background motion.

---

# Slide Specifications

---

## Slide 01

Type: Brand Logo Animation Intro  
Reference: `references/slide_01.jpg`  
Background: Video itself with white background  
Video: `assets/videos/atf-logo-animation.mp4`

Behavior:

* Autoplay when active.
* Play once.
* Do not loop.
* Hold final frame.

Fallback:

```text
assets/logos/logo-atf-black.svg
```

---

## Slide 02

Type: Full Bleed Image + Logo + Hero Text  
Reference: `references/slide_02.jpg`  
Background: `assets/images/slide-2-image-bg.jpg`

Logo:

```text
Asset: assets/logos/logo-atf-white.svg
X: 64
Y: 64
```

Text:

```text
Text: Fintech para negócios
Style: TEXTO_GGG / text-display-large
Color: White
X: 51
Y: 736
W: 1146
H: 280
```

---

## Slide 03

Type: Full Bleed Image + Text  
Reference: `references/slide_03.jpg`  
Background: `assets/images/slide-3-image-bg.jpg`  
Footer Symbol: White standard ATF symbol

Text:

```text
Text: Empreender é avançar diante do incerto.
Style: TEXTO_GG / text-display-medium
Color: White
X: 64
Y: 375
W: 880
H: 330
```

---

## Slide 04

Type: Full Bleed Image + Text  
Reference: `references/slide_04.jpg`  
Background: `assets/images/slide-4-image-bg.jpg`  
Footer Symbol: White standard ATF symbol

Text:

```text
Text: E é justamente por isso que a confiança precisa estar no centro de tudo.
Style: TEXTO_GG / text-display-medium
Color: White
X: 64
Y: 320
W: 1066
H: 440
```

---

## Slide 05

Type: White Background + Text + Highlights  
Reference: `references/slide_05.jpg`  
Background: White  
Footer Symbol: Black standard ATF symbol

Text:

```text
Text: Integramos fundos, crédito e infraestrutura financeira digital para empresas que precisam crescer com critério, governança e previsibilidade.
Style: TEXTO_GG / text-display-medium
Color: Black
X: 64
Y: 265
W: 1730
H: 550
```

Highlights: use `highlightMap[5]`.

---

## Slide 06

Type: White Background + Text + Highlights  
Reference: `references/slide_06.jpg`  
Background: White  
Footer Symbol: Black standard ATF symbol

Text:

```text
Text: A ATF não busca qualquer negócio. Busca os negócios certos — aqueles em que a relação pode ser construída com responsabilidade, clareza e visão de longo prazo.
Style: TEXTO_GG / text-display-medium
Color: Black
X: 64
Y: 210
W: 1604
H: 660
```

Highlights: use `highlightMap[6]`.

---

## Slide 07

Type: Animated Illustration Background + Text + Highlight  
Reference: `references/slide_07.jpg`  
Background: White + full-canvas animated illustration video  
Video: `assets/videos/slide-7-animation-background.mp4`  
Footer Symbol: Black standard ATF symbol

Text:

```text
Text: Escolhemos com quem operar, estruturamos cada solução com rigor e acompanhamos de perto o que colocamos em movimento.
Style: TEXTO_M / text-statement-medium
Color: Black
X: 64
Y: 300
W: 923
H: 480
```

Highlights: use `highlightMap[7]`.

---

## Slide 08

Type: Full Bleed Image + Text  
Reference: `references/slide_08.jpg`  
Background: `assets/images/slide-8-image-bg.jpg`  
Footer Symbol: White standard ATF symbol

Text:

```text
Text: Desde 1997 construindo relações que resistem ao tempo.
Style: TEXTO_GG / text-display-medium
Color: White
X: 64
Y: 375
W: 1344
H: 330
```

---

## Slide 09

Type: Animated Illustration Background + Text + Highlights  
Reference: `references/slide_09.jpg`  
Background: White + full-canvas animated illustration video  
Video: `assets/videos/slide-9-animation-background.mp4`  
Footer Symbol: Black standard ATF symbol

Text:

```text
Text: Nesse tempo, estruturamos milhares de operações e construímos relações que resistem porque escolhemos criteriosamente com quem caminhamos lado a lado.
Style: TEXTO_M / text-statement-medium
Color: Black
X: 67
Y: 300
W: 1110
H: 480
```

Highlights: use `highlightMap[9]`.

---

## Slide 10

Type: Full Bleed Image + Text  
Reference: `references/slide_10.jpg`  
Background: `assets/images/slide-10-image-bg.jpg`  
Footer Symbol: White standard ATF symbol

Text:

```text
Text: Três valores. Uma mesma disciplina.
Style: TEXTO_GG / text-display-medium
Color: White
X: 64
Y: 375
W: 1140
H: 330
```

---

## Slide 11

Type: Full Bleed Image + Text  
Reference: `references/slide_11.jpg`  
Background: `assets/images/slide-11-image-bg.jpg`  
Footer Symbol: White standard ATF symbol

Text:

```text
Text: Confiança
Style: TEXTO_GG / text-display-medium
Color: White
X: 64
Y: 485
W: 887
H: 110
```

---

## Slide 12

Type: White Background + Subtitle + Text + Highlight  
Reference: `references/slide_12.jpg`  
Background: White  
Footer Symbol: Black standard ATF symbol

Subtitle:

```text
Text: O que dizemos, fazemos
Style: TEXTO_P / text-statement-small
Color: Black
X: 64
Y: 141
W: 887
H: 70
```

Main Text:

```text
Text: Respeitamos cada compromisso assumido. Selecionamos parceiros com critério — e reconhecemos a responsabilidade dessa escolha. Confiança não é apenas um atributo de negócio; é o alicerce de cada operação.
Style: TEXTO_G / text-statement-large
Color: Black
X: 64
Y: 332
W: 1754
H: 576
```

Highlights: use `highlightMap[12]`.

---

# Slide Content Configuration — Current Production Map

The following JavaScript-style map reflects the currently documented slide content. It can be used as the basis for generating the production HTML.

```js
const slideContentMap = {
  5: {
    type: "white-text-highlight",
    textBlocks: [
      {
        text: "Integramos fundos, crédito e infraestrutura financeira digital para empresas que precisam crescer com critério, governança e previsibilidade.",
        style: "text-display-medium",
        figmaStyle: "TEXTO_GG",
        color: "black",
        x: 64,
        y: 265,
        width: 1730,
        height: 550
      }
    ]
  },

  6: {
    type: "white-text-highlight",
    textBlocks: [
      {
        text: "A ATF não busca qualquer negócio. Busca os negócios certos — aqueles em que a relação pode ser construída com responsabilidade, clareza e visão de longo prazo.",
        style: "text-display-medium",
        figmaStyle: "TEXTO_GG",
        color: "black",
        x: 64,
        y: 210,
        width: 1604,
        height: 660
      }
    ]
  },

  7: {
    type: "animated-illustration-background-text-highlight",
    video: "assets/videos/slide-7-animation-background.mp4",
    textBlocks: [
      {
        text: "Escolhemos com quem operar, estruturamos cada solução com rigor e acompanhamos de perto o que colocamos em movimento.",
        style: "text-statement-medium",
        figmaStyle: "TEXTO_M",
        color: "black",
        x: 64,
        y: 300,
        width: 923,
        height: 480
      }
    ]
  },

  8: {
    type: "image-background-text",
    background: "assets/images/slide-8-image-bg.jpg",
    textBlocks: [
      {
        text: "Desde 1997 construindo relações que resistem ao tempo.",
        style: "text-display-medium",
        figmaStyle: "TEXTO_GG",
        color: "white",
        x: 64,
        y: 375,
        width: 1344,
        height: 330
      }
    ]
  },

  9: {
    type: "animated-illustration-background-text-highlight",
    video: "assets/videos/slide-9-animation-background.mp4",
    textBlocks: [
      {
        text: "Nesse tempo, estruturamos milhares de operações e construímos relações que resistem porque escolhemos criteriosamente com quem caminhamos lado a lado.",
        style: "text-statement-medium",
        figmaStyle: "TEXTO_M",
        color: "black",
        x: 67,
        y: 300,
        width: 1110,
        height: 480
      }
    ]
  },

  10: {
    type: "image-background-text",
    background: "assets/images/slide-10-image-bg.jpg",
    textBlocks: [
      {
        text: "Três valores. Uma mesma disciplina.",
        style: "text-display-medium",
        figmaStyle: "TEXTO_GG",
        color: "white",
        x: 64,
        y: 375,
        width: 1140,
        height: 330
      }
    ]
  },

  11: {
    type: "image-background-text",
    background: "assets/images/slide-11-image-bg.jpg",
    textBlocks: [
      {
        text: "Confiança",
        style: "text-display-medium",
        figmaStyle: "TEXTO_GG",
        color: "white",
        x: 64,
        y: 485,
        width: 887,
        height: 110
      }
    ]
  },

  12: {
    type: "white-subtitle-text-highlight",
    textBlocks: [
      {
        role: "subtitle",
        text: "O que dizemos, fazemos",
        style: "text-statement-small",
        figmaStyle: "TEXTO_P",
        color: "black",
        x: 64,
        y: 141,
        width: 887,
        height: 70
      },
      {
        role: "main",
        text: "Respeitamos cada compromisso assumido. Selecionamos parceiros com critério — e reconhecemos a responsabilidade dessa escolha. Confiança não é apenas um atributo de negócio; é o alicerce de cada operação.",
        style: "text-statement-large",
        figmaStyle: "TEXTO_G",
        color: "black",
        x: 64,
        y: 332,
        width: 1754,
        height: 576
      }
    ]
  }
};
```

---

# Navigation

Keyboard support:

* Left Arrow = Previous Slide
* Right Arrow = Next Slide
* Spacebar = Next Slide

Optional controls:

* On-screen next/previous controls.
* Progress indicator.
* Fullscreen button.

---

# Presentation Behavior

* Desktop-first.
* Target resolution: 1920x1080.
* Fullscreen presentation mode.
* No scroll.
* One slide visible at a time.
* Smooth slide transitions.
* Videos should reset/play when their slide becomes active.
* Videos should pause when their slide is inactive, unless preloading requires otherwise.

---

# Fidelity Requirements

The HTML version should preserve:

* Typography scale.
* Layout proportions.
* Positioning.
* Margins.
* Visual hierarchy.
* Image composition.
* Overall rhythm of the Figma reference.
* Premium pacing of motion and transitions.

---

# Production Success Criteria

The full HTML version is considered successful when:

* All 52 slides visually match the Figma references.
* All image backgrounds load correctly.
* All animated illustration backgrounds load correctly.
* Logo animations work on slides 01, 23 and 37.
* Product motion works on the relevant slides, starting with Slide 43.
* Keyboard navigation works seamlessly.
* Motion feels premium and smooth.
* Fullscreen mode is functional.
* The codebase is structured as a reusable presentation framework.

---

End of Document
