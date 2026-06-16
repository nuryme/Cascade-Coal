# Cascade & Coal

**Wood-fire steakhouse concept site — Capitol Hill, Seattle.**

A single-page, no-framework website built to the standard of a $10K agency deliverable. Dark-luxury editorial direction, hand-crafted motion, and a typographic identity that feels commissioned rather than templated.

---

**Live Link :** https://cascade-coal.vercel.app

## What It Is

Cascade & Coal is a fictional fine-dining steakhouse brand. The site is a design and front-end exercise — every decision, from the palette to the scroll behaviour, was made to answer one question: *what separates a $200 website from a $10,000 one?*

The answer is taste, restraint, and craft in the details no one consciously notices but everyone feels.

---

## Design

**Direction — Dark Luxury Editorial**
The site commits to a single point of view and doesn't flinch. Near-black backgrounds, an oxblood accent, and brass/copper metallics give it the weight of a Michelin-starred menu. Nothing is generic. Nothing is borrowed from a template.

**Typography**
Cormorant Garamond (display) paired with Barlow (body). Neither is Inter. Neither is Roboto. The display face carries the personality of the brand; the body face keeps it grounded and readable.

**Color System — 5 Semantic Hues**
| Token | Value | Role |
|---|---|---|
| Near-black | `#0D0B09` | Base background |
| Oxblood | `#4E1519` | Deep accent, reserve section |
| Brass | `#C9922B` | Primary accent — labels, borders, CTAs |
| Copper | `#B87333` | Hover/active state of brass |
| Cream | `#F2E8D5` | Primary text |
| Cream-dim | `#BFB09A` | Secondary text |
| Slate | `#6A677A` | Tertiary / metadata text |

Eight tokens, five hues. No rainbow palettes. Premium signals through restraint.

---

## Motion

Every animation was written by hand. No AOS, no GSAP, no scroll libraries.

- **Scroll-driven hero reveal** — clip-path opens from a 25% inset rectangle to full screen as the user scrolls. The video simultaneously zooms out from `scale(1.7)` to `scale(1.0)`. Each headline layer has its own staggered scroll window and parallax drift rate.
- **Ember canvas** — 45 floating particles rendered via `requestAnimationFrame`. Each ember has individual velocity, wobble frequency, opacity arc, and glow. Pauses when the hero leaves the viewport.
- **Story fire** — six radial-gradient heat orbs drifting via sine/cosine paths on a canvas behind the Our Story section. Each orb has a unique parallax depth: mouse movement shifts them at different rates, creating a sense of 3D heat haze.
- **Reserve fire** — same system, brass/copper dominant, orbs sourced from below the frame like firelight rising from a hidden hearth.
- **Custom cursor** — 7px brass dot (position-snapped) + 34px ring (lerp lag at 0.11). Expands on interactive elements.
- **Brass border draw** — menu card top border scales from `scaleX(0)` to `scaleX(1)` on hover, left-to-right, over 0.55s.
- **Center-out underline** — nav link underlines expand symmetrically from center outward.
- **Section dividers** — three hairline rules draw in from center via `scaleX` as they enter the viewport.
- **Breathing glow** — the story visual panel pulses at 7s ease-in-out, cycling opacity 1 → 0.68 → 1.
- All motion respects `prefers-reduced-motion`.

---

## The $10K Checklist

| # | Criterion | Status |
|---|---|---|
| 01 | Point of view, not a template | ✅ |
| 02 | Typography that does work | ✅ |
| 03 | Restrained color system | ✅ |
| 04 | Hierarchy that breathes | ✅ |
| 05 | Imagery with intent | ⚠️ Video hero deliberate; below-fold CSS-only by design |
| 06 | Motion that whispers | ✅ |
| 07 | Mobile that's designed, not shrunk | ✅ |
| 08 | The invisible expensive stuff | ✅ |

---

## Stack

- Pure HTML + embedded CSS + vanilla JS
- No build step. No framework. No dependencies.
- One file: `index.html`
- Google Fonts: Cormorant Garamond + Barlow

---

## Structure

```
index.html
  ├── Nav          fixed, blur-on-scroll, mobile fullscreen overlay
  ├── Hero         scroll-driven clip-path video reveal + ember canvas
  ├── The Cut      6-item menu grid with brass micro-interactions
  ├── Our Story    two-column layout with live fire canvas background
  ├── Reserve      centered CTA on oxblood with parallax fire canvas
  ├── Location     hours table + contact info
  └── Footer
```

---

*Built as a design and engineering exercise. All brand content is fictional.*
