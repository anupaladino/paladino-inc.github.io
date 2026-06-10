# ATF Credentials HTML MVP

Version 1.1

---

# Project Overview

This document defines the structure, assets, typography, layout system and animation direction required to build the first HTML-based version of the ATF Credentials presentation.

The goal of this MVP is to recreate the first 5 slides of the presentation with high visual fidelity to the Figma source file while introducing animation, navigation and multimedia capabilities that are not possible in Figma Slides.

This MVP will serve as the foundation for the complete migration of the credentials presentation to HTML.

---

# Current Folder Structure

```text
atf-credenciais-web
├── assets
│   ├── images
│   │   ├── slide-2-image-bg.jpg
│   │   ├── slide-3-image-bg.jpg
│   │   └── slide-4-image-bg.jpg
│   │
│   ├── logos
│   │   ├── logo-atf-black.svg
│   │   ├── logo-atf-white.svg
│   │   ├── symbol-atf-black.svg
│   │   └── symbol-atf-white.svg
│   │
│   ├── text-highlight-background
│   │   ├── text-highlight-bg-1.png
│   │   └── text-highlight-bg-2.png
│   │
│   └── videos
│       └── atf-logo-animation.mov
│
├── references
│   ├── Slide 1.jpg
│   ├── Slide 2.jpg
│   ├── Slide 3.jpg
│   ├── Slide 4.jpg
│   └── Slide 5.jpg
│
└── slides
    └── slides-file-brief.md
```

---

# Objectives

The HTML presentation should:

* Preserve the visual quality of the Figma design
* Support videos and motion assets
* Support richer animations and transitions
* Allow fullscreen presentation mode
* Be optimized for desktop presentations
* Become the foundation for future ATF institutional presentations

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

## Display Large

Used on Slide 02.

Font Family:
Plus Jakarta Sans

Font Weight:
Medium (500)

Font Size:
164px

Line Height:
140px

Letter Spacing:
-1%

Alignment:
Left

Color:
#FFFFFF

---

## Display Medium

Used on Slides 03, 04 and 05.

Font Family:
Plus Jakarta Sans

Font Weight:
Bold (700)

Font Size:
108px

Line Height:
110px

Letter Spacing:
-1%

Alignment:
Left

Color:
#FFFFFF on image slides

#000000 on white background slides

---

# Colors

## White

#FFFFFF

## Black

#000000

## Highlight Gold

Use exported Figma assets:

```text
../assets/text-highlight-background/text-highlight-bg-1.png
../assets/text-highlight-background/text-highlight-bg-2.png
```

---

# Asset Paths

All paths below are relative to:

```text
/slides/slides-file-brief.md
```

## Images

```text
../assets/images/slide-2-image-bg.jpg
../assets/images/slide-3-image-bg.jpg
../assets/images/slide-4-image-bg.jpg
```

## Logos

```text
../assets/logos/logo-atf-black.svg
../assets/logos/logo-atf-white.svg
../assets/logos/symbol-atf-black.svg
../assets/logos/symbol-atf-white.svg
```

## Highlight Backgrounds

```text
../assets/text-highlight-background/text-highlight-bg-1.png
../assets/text-highlight-background/text-highlight-bg-2.png
```

## Video

```text
../assets/videos/atf-logo-animation.mov
```

## References

```text
../references/Slide 1.jpg
../references/Slide 2.jpg
../references/Slide 3.jpg
../references/Slide 4.jpg
../references/Slide 5.jpg
```

---

# Slide Specifications

---

# Slide 01

## Type

Logo Animation Intro

## Reference

../references/Slide 1.jpg

## Background

The slide uses the video itself as the visual asset.

The video already contains a white background, so no additional background layer is required.

## Asset

../assets/videos/atf-logo-animation.mov

## Layout

The video should be centered both horizontally and vertically on the canvas.

Canvas:

1920x1080

Video Position:

Horizontal center

Vertical center

## Behavior

The video should autoplay when the slide becomes active.

The video should play once.

The video should not loop.

The video should remain on the final frame after playback.

## Fallback

If the video cannot be loaded, use:

../assets/logos/logo-atf-black.svg

Fallback behavior:

Static logo centered on the slide.

## Transition

Fade in.

Duration:
1.0s

---

# Slide 02

## Type

Full Bleed Image

## Reference

```text
../references/Slide 2.jpg
```

## Background

```text
../assets/images/slide-2-image-bg.jpg
```

## Assets

```text
../assets/logos/logo-atf-white.svg
```

## Logo Position

Top:
64px

Left:
64px

## Title

Fintech para negócios

## Typography

Display Large

## Position

X = 51

Y = 736

## Text Box

Width = 1146

Height = 280

## Animation Direction

1. Background fade-in
2. Logo fade-in
3. Title fade + rise 20px

---

# Slide 03

## Type

Full Bleed Image

## Reference

```text
../references/Slide 3.jpg
```

## Background

```text
../assets/images/slide-3-image-bg.jpg
```

## Assets

```text
../assets/logos/symbol-atf-white.svg
```

## Symbol Position

Left:
64px

Bottom:
64px

## Title

Empreender é avançar diante do incerto.

## Typography

Display Medium

## Position

X = 64

Y = 375

## Text Box

Width = 880

Height = 330

## Animation Direction

1. Background fade-in
2. Text reveal
3. Symbol fade-in

---

# Slide 04

## Type

Full Bleed Image

## Reference

```text
../references/Slide 4.jpg
```

## Background

```text
../assets/images/slide-4-image-bg.jpg
```

## Assets

```text
../assets/logos/symbol-atf-white.svg
```

## Symbol Position

Left:
64px

Bottom:
64px

## Title

E é justamente por isso que a confiança precisa estar no centro de tudo.

## Typography

Display Medium

## Position

X = 64

Y = 320

## Text Box

Width = 1066

Height = 440

## Animation Direction

1. Background fade-in
2. Text reveal
3. Symbol fade-in

---

# Slide 05

## Type

Editorial Statement

## Reference

```text
../references/Slide 5.jpg
```

## Background

White

## Assets

```text
../assets/logos/symbol-atf-black.svg
../assets/text-highlight-background/text-highlight-bg-1.png
../assets/text-highlight-background/text-highlight-bg-2.png
```

## Symbol Position

Left:
64px

Bottom:
64px

## Title

A ATF integra fundos, crédito e infraestrutura financeira digital para empresas que precisam crescer com critério, governança e previsibilidade.

## Typography

Display Medium

## Position

X = 64

Y = 265

## Text Box

Width = 1730

Height = 550

## Text Color

#000000

---

## Highlight Assets

### Highlight 01

Asset:

```text
../assets/text-highlight-background/text-highlight-bg-1.png
```

Position:

X = 718

Y = 605

---

### Highlight 02

Asset:

```text
../assets/text-highlight-background/text-highlight-bg-2.png
```

Position:

X = 50

Y = 714

---

## Animation Direction

1. Text reveal
2. Highlight 01 grows horizontally
3. Highlight 02 grows horizontally
4. Final hold

---

# Navigation

For MVP:

* Arrow Left
* Arrow Right

Keyboard support:

* Left Arrow
* Right Arrow

Optional:

* Spacebar = Next Slide

---

# Presentation Behavior

Desktop only in Phase 1.

Target Resolution:

1920x1080

Fullscreen presentation mode.

No scroll.

One slide visible at a time.

Smooth slide transitions.

---

# Fidelity Requirements

The HTML version should preserve:

* Typography scale
* Layout proportions
* Positioning
* Margins
* Visual hierarchy
* Image composition
* Overall rhythm of the Figma reference

The goal is to recreate the Figma file as accurately as possible while introducing motion and interaction capabilities.

---

# MVP Success Criteria

The MVP is considered successful when:

* Slides 01–05 visually match the Figma source
* Navigation works seamlessly
* Motion feels premium and smooth
* Assets load correctly
* Fullscreen presentation mode is functional
* The structure is reusable for the remaining slides

---

End of Document
