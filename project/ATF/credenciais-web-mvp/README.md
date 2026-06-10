# ATF Credentials Web

## Overview

This repository contains the assets, references and implementation brief for an experimental HTML version of the ATF Credentials presentation.

The original presentation was designed in Figma and later evaluated for migration to Figma Slides. During testing, we identified limitations related to animation capabilities, video handling and overall presentation flexibility.

This project explores an alternative approach: rebuilding the presentation as an HTML-based experience that preserves the visual quality of the original design while introducing richer animations, motion assets and presentation controls.

---

## Current Scope

This MVP focuses exclusively on recreating the first five slides of the presentation.

The objective is to validate:

* Design fidelity
* Typography implementation
* Layout system
* Motion behavior
* Video integration
* Navigation model
* Presentation performance

Once validated, the same system can be expanded to support the complete credentials presentation.

---

## Source Material

The project is based on:

* Original Figma Design file
* Motion assets developed for ATF
* Exported slide references
* Design system specifications documented in the project brief

---

## Folder Structure

```text
atf-credenciais-web
├── assets
│   ├── images
│   ├── logos
│   ├── text-highlight-background
│   └── videos
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

## Key Documents

### slides/slides-file-brief.md

Primary project specification.

Contains:

* Canvas setup
* Grid system
* Typography specifications
* Asset references
* Slide-by-slide breakdown
* Animation direction
* Navigation requirements
* Fidelity requirements

This document should be treated as the source of truth during implementation.

---

## Design System

### Canvas

* 1920 × 1080
* 16:9 aspect ratio

### Grid

* 16 Columns
* 11 Rows
* 64px Margin
* 32px Gutter

### Typography

Primary typeface:

* Plus Jakarta Sans

---

## MVP Slides

### Slide 01

Logo animation intro.

### Slide 02

Hero statement:
"Fintech para negócios"

### Slide 03

Manifesto statement:
"Empreender é avançar diante do incerto."

### Slide 04

Manifesto statement:
"E é justamente por isso que a confiança precisa estar no centro de tudo."

### Slide 05

Institutional positioning statement with highlighted keywords.

---

## Technical Direction

The HTML version should:

* Match the Figma design as closely as possible
* Support motion assets and videos
* Run in fullscreen presentation mode
* Support keyboard navigation
* Maintain premium visual quality
* Be optimized primarily for desktop presentations

---

## Long-Term Vision

The objective is not simply to recreate a presentation.

The goal is to establish a reusable presentation framework for ATF, capable of combining:

* Editorial layouts
* Motion assets
* Video content
* Interactive navigation
* Future presentation updates

This MVP serves as the first validation step toward that system.

---

## Status

Current Phase:

Design System Documentation + MVP Preparation

Slides Included:

* Slide 01
* Slide 02
* Slide 03
* Slide 04
* Slide 05

Next Phase:

HTML implementation and animation testing.
