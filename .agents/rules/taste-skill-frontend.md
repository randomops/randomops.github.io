---
trigger: model_decision
description: Anti-slop frontend and UI design standards based on Taste Skill (tasteskill.dev).
---

# Taste Skill: Anti-Slop Frontend & UI Design Standards

All frontend, HTML, CSS/Tailwind, React, Next.js, and template styling must adhere to the **Taste Skill Framework** (`https://tasteskill.dev`).

## 1. Zero AI Slop (Anti-Default Discipline)
Strictly banned default AI aesthetics:
- ❌ Centered hero text floating over purple/indigo dark mesh gradients.
- ❌ Three identical floating feature cards with generic rounded icons.
- ❌ Flat, uninspired `Inter` + `slate-900` boilerplates without typographic character.
- ❌ Generic, unstyled glassmorphism / excessive backdrop blur without purpose.
- ❌ Infinite loop micro-animations that distract from readability.
- ❌ Hand-rolled div-based fake screenshots / mocked dashboards.

## 2. Mandatory One-Line "Design Read"
Before modifying or creating any frontend UI components, output a one-line Design Read:
> `Reading this as: <page kind> for <audience>, with a <vibe> language, leaning toward <design system or aesthetic family>.`

## 3. The Three Dials Calibration
Calibrate global parameters for every UI surface:
- **`DESIGN_VARIANCE`** (1–10): *Layout experimentation & asymmetry* (Default: `7` or `8`)
- **`MOTION_INTENSITY`** (1–10): *Micro-interactions & animation energy* (Default: `5` or `6`)
- **`VISUAL_DENSITY`** (1–10): *Information density vs. airy negative space* (Default: `4`)

## 4. Strict UI & Accessibility Guardrails
- **Hero Viewport Fit**: Hero must fit initial viewport (`min-h-[100dvh]`). Max 2 lines headline, max 20 words subtext.
- **Hero Top Padding Cap**: Max `pt-24` (≈6rem) on desktop.
- **Nav Single Line**: Navigation must render on a single line on desktop (max height 80px).
- **Eyebrow Restraint**: Maximum 1 small-caps eyebrow label per 3 sections.
- **Button & Form Contrast**: Strict WCAG AA compliance (4.5:1 minimum contrast). Never wrap CTA text at desktop.
- **Reduced Motion**: All animations above `MOTION_INTENSITY > 3` must honor `prefers-reduced-motion`.
